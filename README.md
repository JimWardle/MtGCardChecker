# 🃏 MTG Card Pricing Tool

A web-based tool for cataloging and pricing Magic: The Gathering cards using the Scryfall API.

## 🌟 Features

- **Card Name Parsing**: Enter card names, one per line
- **Set-Specific Pricing**: Optional set code support for accurate vintage card pricing
- **Real-Time API Integration**: Queries Scryfall API with proper rate limiting
- **Sortable Results**: Click any column header to sort
- **Export Options**: 
  - Export to CSV for Excel/Google Sheets
  - Copy to clipboard functionality
- **Price Statistics**: View total collection value, card count, and average price
- **Rarity Color Coding**: Visual indicators for Common, Uncommon, Rare, and Mythic
- **Error Handling**: Graceful handling of missing cards or API issues

## 🚀 Live Demo

[View Live Tool](https://jimwardle.github.io/MtGCardChecker/) 
📋 How to Use

### Basic Usage

1. Enter card names in the text area, one per line:
```
Lightning Bolt
Path to Exile
Sol Ring
```

2. Click "Fetch Prices" to query the Scryfall API
3. View results in the sortable table
4. Export to CSV or copy to clipboard

### Advanced Usage: Set Codes

For accurate pricing of specific printings, add set codes in brackets:

```
Lightning Bolt [LEA]
Path to Exile [OTC]
Sol Ring [CMR]
```

**Without set codes**: Returns most recent printing
**With set codes**: Returns specific printing from that set

### Common Set Codes

**Vintage Sets (High Value)**:
- `LEA` - Limited Edition Alpha (1993)
- `LEB` - Limited Edition Beta (1993)
- `2ED` - Unlimited Edition
- `3ED` - Revised Edition
- `ARN` - Arabian Nights (1993)
- `ATQ` - Antiquities (1994)
- `LEG` - Legends (1994)

**Modern Sets**:
- `KLD` - Kaladesh
- `CMR` - Commander Legends
- `MH2` - Modern Horizons 2
- `OTC` - Outlaws of Thunder Junction Commander

[Full list of set codes on Scryfall](https://scryfall.com/sets)

## 🛠️ Installation

### Option 1: GitHub Pages (Recommended)

1. Fork this repository
2. Go to Settings → Pages
3. Select "Deploy from branch" → main branch
4. Your site will be live at `https://yourusername.github.io/mtg-card-pricer/`

### Option 2: Local Usage

1. Download `index.html`
2. Open directly in your web browser
3. No installation or dependencies required!

## 📸 Workflow for Physical Card Collections

### Step 1: Photograph Cards
- Arrange 10-15 cards in rows
- Ensure card names are clearly visible
- Good lighting, avoid glare
- Straight-on angle works best

### Step 2: Parse Card Names
Use Claude or manual entry to identify card names from photos.

### Step 3: Identify Sets (Optional but Recommended)
- **Modern cards**: Look at bottom of card for 3-letter set code
- **Older cards**: Identify set symbol (small icon on middle-right)
- **Very old cards** (pre-1995): May have no set symbol - research needed

### Step 4: Enter and Price
Paste card list into tool, run pricing, export results.

### Step 5: Flag for Research
Cards showing $0.00 or suspiciously low prices may need manual verification, especially:
- Cards with old card frames (pre-2003)
- Vintage printings vs modern reprints
- Reserved List cards

## 🎯 Use Cases

### For Collectors
- Quickly value your collection
- Identify valuable cards worth protecting
- Track collection value over time
- Export to spreadsheets for insurance purposes

### For Deck Builders
- Price out deck lists before buying
- Compare prices across different printings
- Find budget alternatives

### For Sellers
- Bulk price cards for listing
- Identify high-value cards to sell individually
- Export pricing data for inventory management

## ⚠️ Important Notes

### Pricing Accuracy
- Prices from Scryfall represent market averages
- Actual selling prices vary by condition
- Vintage cards: Tool may show recent reprint prices if set code not specified
- Some rare cards show $0.00 (no market data available)

### Set Code Identification
**Always specify set codes for vintage cards!**

Example price differences:
- Lightning Bolt (Alpha): ~$350
- Lightning Bolt (Modern reprint): ~$1

Without set codes, you'll see the modern price even if you own the valuable Alpha version.

### Rate Limiting
- Tool includes 100ms delay between requests
- Respects Scryfall API guidelines
- Large collections (100+ cards) will take time to process

## 🔧 Technical Details

### Built With
- Pure HTML/CSS/JavaScript
- Scryfall API
- No external dependencies
- Runs entirely in browser

### API Endpoints Used
- `/cards/named?exact={name}` - Most recent printing
- `/cards/named?exact={name}&set={code}` - Specific printing

### Browser Compatibility
- Chrome/Edge (recommended)
- Firefox
- Safari
- Any modern browser with JavaScript enabled

## 📊 Future Enhancement Ideas

- [ ] Bulk image upload and OCR for card names
- [ ] Set symbol recognition from photos
- [ ] Price history tracking
- [ ] Deck building recommendations
- [ ] Integration with collection management platforms
- [ ] Multi-language support
- [ ] Condition adjustment factors

## 🤝 Contributing

This is a personal project, but suggestions and improvements are welcome!

## 📝 License

Free to use for personal and commercial purposes. Card data and pricing provided by Scryfall.

## 🙏 Acknowledgments

- [Scryfall](https://scryfall.com/) for the excellent API
- Wizards of the Coast for Magic: The Gathering
- The MTG community for set identification resources

## 💬 Prompt for Future Chats

If you want to continue working on this project in a new chat, use this prompt:

```
I have a Magic: The Gathering card pricing tool that uses the Scryfall API. 
It's a single HTML file that:
- Takes card names (one per line)
- Supports optional set codes in brackets like "Lightning Bolt [LEA]"
- Queries Scryfall API for pricing data
- Displays results in a sortable table
- Exports to CSV

Current features: [list current features]
I'd like to: [describe what you want to add/modify]

The tool is hosted on GitHub Pages at: [your URL]
```

## 📞 Support

For issues with:
- **This tool**: Open a GitHub issue
- **Scryfall API**: Check [Scryfall API docs](https://scryfall.com/docs/api)
- **Card identification**: Post in MTG communities with photos

---

**Happy Cataloging!** 🎴✨

*Built with ❤️ for the Magic: The Gathering community*
