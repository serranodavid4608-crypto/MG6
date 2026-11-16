# MG6
## DevLog
1. If we write a loop in a update method it will complete before the update method finish that will result a lag or even a freeze due to loop be compete in the entire in single frame.
2. The issue with our logic is that player's collider will turn back on mid-jump if they don't clear the platform before reaching the peak of their jump the logic allow this because it relies strictly on vertical velocity that can lead to stuck inside the platform and other things this also happen by that unity physical engine detects two active colliders overlapping each other, it immediately tries to separate that usually result to the dynamic rigidbody get push out then the static collider.
