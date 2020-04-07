Bread Loader - README

I figured out how to use Lottie in Swift. Commented out below.

---- BELOW ----



//
//  ViewController.swift
//  BreadLoader
//
//  Created by Tim Darragh on 4/2/20.
//  Copyright © 2020 Tim Darragh. All rights reserved.
//

import UIKit
import Lottie

class ViewController: UIViewController {

    // container for animation to play
    @IBOutlet private var animationView: AnimationView!

    @IBOutlet var shape: AnimationView!

    override func viewDidLoad() {
        super.viewDidLoad()
        // Do any additional setup after loading the view.

        startAnimation()
        showShape()
    }

    // load animation, scale in container, loop and play
    func startAnimation() {
        animationView.animation = Animation.named("loaderColors")
        animationView.contentMode = .scaleAspectFit
        animationView.loopMode = .loop
        animationView.play()
    }

    // load animation, scale in container, loop and play
    func showShape() {
        shape.animation = Animation.named("shape1F")
        shape.contentMode = .scaleAspectFit
        shape.loopMode = .loop
        animationView.play()
    }


}
