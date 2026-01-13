# 🧪 Test URLs for Stream Integration

## ✅ Ready-to-Use Test URLs

### Direct Audio Streams (MP3)
```
https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3
https://www.soundhelix.com/examples/mp3/SoundHelix-Song-2.mp3
https://www.soundhelix.com/examples/mp3/SoundHelix-Song-3.mp3
https://www.soundhelix.com/examples/mp3/SoundHelix-Song-4.mp3
https://www.soundhelix.com/examples/mp3/SoundHelix-Song-5.mp3
https://www.soundhelix.com/examples/mp3/SoundHelix-Song-6.mp3
https://www.soundhelix.com/examples/mp3/SoundHelix-Song-7.mp3
https://www.soundhelix.com/examples/mp3/SoundHelix-Song-8.mp3
https://www.soundhelix.com/examples/mp3/SoundHelix-Song-9.mp3
https://www.soundhelix.com/examples/mp3/SoundHelix-Song-10.mp3
```

**Test:** All controls + EQ features work! ✅

---

### HLS Streams (.m3u8)
```
https://test-streams.mux.dev/x36xhzz/x3iqsled.m3u8
https://test-streams.mux.dev/x36xhzz/zc0p4wck.m3u8
https://test-streams.mux.dev/x36xhzz/5hlzts3j.m3u8
```

**Test:** HLS streaming with adaptive bitrate ✅

---

### YouTube Videos (Embed Mode)
```
https://youtu.be/dQw4w9WgXcQ
https://youtu.be/jNQXAC9IVRw
https://youtu.be/9bZkp7q19f0
https://youtu.be/ZXsQAXx_ao0
https://youtu.be/YQHsXMglC9A
https://youtu.be/L_jWHffIx5E
https://youtu.be/CVi_SQhI6I0
```

**Test:** Video embed with play/pause/volume ✅

---

### Spotify Tracks (Embed Widget)
```
https://open.spotify.com/track/11dFghVXANMlKmJXsNCQvb
https://open.spotify.com/track/4cOdK2wGLETKBW3PvgPWqV
https://open.spotify.com/track/1301WleyT98MSxVHPZCA6M
https://open.spotify.com/track/5yzHe8fqKrpQfDpZ8sKvGi
```

**Test:** Spotify widget preview (basic playback) ✅

---

## 🎯 Testing Sequence

### Step 1: Test Direct Audio (Best Features)
1. Add: `https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3`
2. Test controls:
   - ▶️ Play/Pause
   - ⏩ Forward 10s
   - ⏪ Rewind 10s
   - ⏱️ Click on progress bar to seek
   - 🔊 Volume slider
   - ⚡ Playback speed buttons
3. Test audio:
   - 🎛️ Equalizer
   - 🔊 Bass control
   - ✨ Treble control
4. Verify: Check 🌐 Streams tab shows the song

### Step 2: Test HLS Stream
1. Add: `https://test-streams.mux.dev/x36xhzz/x3iqsled.m3u8`
2. Verify HLS loads (look for "HLS stream attached" in console)
3. Test same controls as Step 1

### Step 3: Test YouTube Embed
1. Add: `https://youtu.be/dQw4w9WgXcQ`
2. Should show video player
3. Test:
   - ▶️ Play/Pause button in player controls
   - 🔊 Volume slider
   - ⚡ Speed selector
   - ▶️ Video player's built-in controls
4. Note: EQ won't work (expected for embeds)

### Step 4: Test Stream Library
1. Add 2-3 more streams
2. Go to 🌐 Streams tab
3. Click on any stream to play
4. Test:
   - ⏭️ Next button (plays next stream)
   - ⏮️ Previous button (plays previous stream)
   - 🗑️ Delete button

### Step 5: Test Switching
1. Load a local music file
2. Play a stream from 🌐 Streams tab
3. Go back to 🎵 Songs tab and play a song
4. Go back to 🌐 Streams tab and play stream
5. Verify: Controls work with both seamlessly

---

## 🔍 Debugging Tips

### Check Console (F12):
```javascript
// Should see these success messages:
✅ "HLS stream attached"
✅ "Direct audio URL set"
✅ "Now Playing updated"
✅ "Stream added to library"
```

### Common Issues:

**"Stream not playing"**
- Check URL is valid (test in new tab)
- Check browser console for errors
- Ensure CORS is allowed

**"EQ not working"**
- EQ only works with direct audio
- Not available for YouTube/Spotify
- Check you're using a .mp3 or .m3u8 URL

**"Next/Previous doesn't work"**
- Add stream with "Add Stream" button (saves to library)
- Then next/previous will navigate through streams

**"Controls feel slow"**
- Refresh page
- Clear browser cache (Ctrl+Shift+Del)
- Try simpler URL first

---

## 📊 Feature Support by Stream Type

### Direct Audio (.mp3)
```
✅ Play/Pause
✅ Next/Previous
✅ Volume
✅ Speed
✅ EQ Equalizer
✅ Bass/Treble
✅ Pre-Amplifier
✅ AI Enhancement
✅ Seek/Progress
```

### HLS Stream (.m3u8)
```
✅ Play/Pause
✅ Next/Previous (through library)
✅ Volume
✅ Speed
✅ EQ Equalizer
✅ Bass/Treble
✅ Seek/Progress
✅ Adaptive Quality
```

### YouTube Embed
```
✅ Play/Pause
✅ Next/Previous (through library)
✅ Volume
✅ Speed
⚠️ Seek/Progress (embed controls)
❌ EQ (not supported)
❌ Bass/Treble (not supported)
```

### Spotify Embed
```
✅ Play/Pause
⚠️ Other controls (limited)
❌ EQ (not supported)
```

---

## 🚀 Deployment Check

Before deploying, test:

1. **Local MP3** - Should have all features
2. **HLS Stream** - Should stream with quality switching
3. **YouTube** - Should show video embed
4. **Stream Library** - Should persist streams
5. **All Controls** - Should respond smoothly

Then **deploy to Netlify/Vercel** and test again with HTTPS domain.

---

## 📝 Pro Tips

### For Best Testing:
- Use SoundHelix MP3s (reliable, free)
- Test on Chrome first
- Open DevTools (F12) to see console logs
- Keep console clean - errors show quickly

### Adding Your Own Streams:
- Copy your stream URL
- Paste in the input field
- Click ➕ Add Stream
- Test all controls
- Delete if needed

### Performance Notes:
- Large HLS files may take time to load
- First play might buffer - normal
- Refresh page if controls lag
- Check network tab for failed requests

---

## ✅ Checklist Before Deploy

- [ ] Local MP3 plays with all controls
- [ ] HLS stream loads and plays
- [ ] YouTube video embeds properly
- [ ] Stream library saves and loads
- [ ] Next/Previous works with streams
- [ ] Volume control works
- [ ] Speed control works
- [ ] EQ works on direct audio
- [ ] Progress bar allows seeking
- [ ] No errors in console
- [ ] All tabs work (Songs, Artists, Albums, Recent, Streams)

If all checked ✅ - **Ready to deploy!** 🚀

---

## 🎯 After Deployment

Once on a real domain with HTTPS:

1. Test all URLs again
2. YouTube API will activate
3. All controls will work perfectly
4. Share the domain with users
5. Watch it scale! 📈

**Everything should work exactly as tested!** ✨

