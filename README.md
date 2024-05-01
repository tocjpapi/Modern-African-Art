



https://github.com/tocjpapi/Modern-African-Art/assets/148444308/a723ab34-9b33-49ca-802a-ee365f288a3c


# Modern African Art Showcase

Welcome to the Modern African Art Showcase, a website dedicated to expressing the vibrant beauty and cultural significance of contemporary African art. This platform aims to fill the void in online representation, offering a comprehensive exploration of African artistry as it was meant to be experienced.

## Description

In the vast landscape of online platforms, there's a noticeable absence of spaces that truly encapsulate the essence of modern African art. This project was born out of a desire to rectify this oversight and provide a digital haven where the richness and diversity of African artistic expression can flourish.

## Getting Started

### Dependencies

To access the Modern African Art Showcase, you'll need:
- A good web browser
- Internet connectivity

### Text Reveal Animation

```
<script>
    const textReveals = document.querySelectorAll('.text__reveal');
    
    function animateTextReveal(entries) {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                console.log(entry);
                const spans = entry.target.querySelectorAll('span');
                spans.forEach((span, idx) => {
                    setTimeout(() => {
                        span.style.transform = 'translateY(0)';
                    }, (idx + 1) * 50);
                });
    
                let startTime;
                function animate(time) {
                    if (!startTime) startTime = time;
                    const progress = time - startTime;
    
                    spans.forEach((span, idx) => {
                        const delay = (idx + 1) * 50;
                        if (progress > delay) {
                            span.style.transform = 'translateY(0)';
                        }
                    });
    
                    if (progress < spans.length * 50) {
                        requestAnimationFrame(animate);
                    }
                }
    
                requestAnimationFrame(animate);
            }
        });
    }
    
    const options = {
        rootMargin: '0px',
        threshold: 1.0
    };
    
    const observe = new IntersectionObserver(animateTextReveal, options);
    
    textReveals.forEach(text => {
        const string = text.innerText;
        const spans = Array.from(string).map(char => `<span>${char}</span>`).join('');
        text.innerHTML = spans;
        observe.observe(text);
    });
    
</script>
```

### Installation

This project doesn't require any installation. Simply download to start exploring the world of modern African art.

### Executing program

To experience the Modern African Art Showcase:
1. Open your preferred web browser.
2. Navigate to the local file.

## Help

If you encounter any issues or have questions while using the Modern African Art Showcase, Too bad bro I aint redoing this shii.

## Author

- Treasure Onwuchekwa (CJ)
- cjwebdesigned@gmail.com

## Version History

- 1.0
  - There was only one release

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgment
- [CJ](https://www.instagram.com/varmoux/)
