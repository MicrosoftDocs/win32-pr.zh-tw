---
title: 觸控
description: 所有的 Microsoft Windows 應用程式都應該有絕佳的觸控體驗。 建立這類體驗比您想像的簡單。
ms.assetid: a87d0726-1c57-4cf8-9e35-4e73a09ff1a3
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: a44a95ad963d3563418ed0492e55606824011f31
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104566639"
---
# <a name="touch"></a><span data-ttu-id="77443-104">觸控</span><span class="sxs-lookup"><span data-stu-id="77443-104">Touch</span></span>

> [!NOTE]
> <span data-ttu-id="77443-105">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="77443-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="77443-106">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="77443-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="77443-107">所有的 Microsoft Windows 應用程式都應該有絕佳的觸控體驗。</span><span class="sxs-lookup"><span data-stu-id="77443-107">All Microsoft Windows applications should have a great touch experience.</span></span> <span data-ttu-id="77443-108">建立這類體驗比您想像的簡單。</span><span class="sxs-lookup"><span data-stu-id="77443-108">And creating such an experience is easier than you think.</span></span>

<span data-ttu-id="77443-109">觸控指的是使用一或多個手指透過裝置顯示來提供輸入，並與 Windows 和應用程式互動。</span><span class="sxs-lookup"><span data-stu-id="77443-109">Touch refers to using one or more fingers to provide input through a device display and interact with Windows and apps.</span></span> <span data-ttu-id="77443-110">觸控優化應用程式有一個 UI 和互動模型，其設計目的是要容納較大型、較不精確的連絡人區域、觸控裝置的各種外型規格，以及許多做法和掌握使用者在使用觸控裝置時可能採用的程式。</span><span class="sxs-lookup"><span data-stu-id="77443-110">A touch-optimized app has a UI and interaction model designed to accommodate the larger, less precise contact areas of touch, the various form factors of touch devices, and the many postures and grips users might adopt when using a touch device.</span></span>

![使用者使用觸控與平板電腦互動](images/inter_touch_image1.jpeg)

<span data-ttu-id="77443-112">每個輸入裝置都有其優點。</span><span class="sxs-lookup"><span data-stu-id="77443-112">Each input device has its strengths.</span></span> <span data-ttu-id="77443-113">鍵盤最適合用來輸入文字，並為命令提供最少量的手移動。</span><span class="sxs-lookup"><span data-stu-id="77443-113">The keyboard is best for text input and giving commands with minimal hand movement.</span></span> <span data-ttu-id="77443-114">滑鼠最適合有效率、精確的指標。</span><span class="sxs-lookup"><span data-stu-id="77443-114">The mouse is best for efficient, precise pointing.</span></span> <span data-ttu-id="77443-115">觸控最適合用於物件操作並提供簡單的命令。</span><span class="sxs-lookup"><span data-stu-id="77443-115">Touch is best for object manipulation and giving simple commands.</span></span> <span data-ttu-id="77443-116">畫筆最適合用於自由格式的運算式，如同手寫和繪圖。</span><span class="sxs-lookup"><span data-stu-id="77443-116">A pen is best for freeform expression, as with handwriting and drawing.</span></span>

<span data-ttu-id="77443-117">Windows 8.1 已針對回應性、準確度和易用性進行優化，同時完全支援傳統的輸入方法， (例如滑鼠、畫筆和鍵盤) 。</span><span class="sxs-lookup"><span data-stu-id="77443-117">Windows 8.1 is optimized for responsiveness, accuracy, and ease of use with touch while fully supporting traditional input methods (such as mouse, pen, and keyboard).</span></span> <span data-ttu-id="77443-118">傳統輸入模式所提供的速度、精確度和 tactile 意見反應，對許多使用者來說都很熟悉且吸引人，而且可能更適合特定的互動案例。</span><span class="sxs-lookup"><span data-stu-id="77443-118">The speed, accuracy, and tactile feedback that traditional input modes provide are familiar and appealing to many users and potentially better suited to specific interaction scenarios.</span></span>

<span data-ttu-id="77443-119">您可以在個別主題中找到與滑鼠、畫筆和協助工具相關的指導方針。</span><span class="sxs-lookup"><span data-stu-id="77443-119">You can find guidelines related to mouse, pen, and accessibility in separate topics.</span></span>

<span data-ttu-id="77443-120">當您考慮應用程式的互動體驗時：</span><span class="sxs-lookup"><span data-stu-id="77443-120">When you think about the interaction experience for your app:</span></span>

<span data-ttu-id="77443-121">請勿假設 UI 適用于滑鼠，也適用于觸控。</span><span class="sxs-lookup"><span data-stu-id="77443-121">Don't assume that if a UI works well for a mouse, it also works well for touch.</span></span> <span data-ttu-id="77443-122">雖然良好的滑鼠支援是一開始，但良好的觸控體驗有一些額外的需求。</span><span class="sxs-lookup"><span data-stu-id="77443-122">While good mouse support is a start, a good touch experience has a few additional requirements.</span></span>

<span data-ttu-id="77443-123">請假設，如果 UI 適用于手指，也適用于畫筆。</span><span class="sxs-lookup"><span data-stu-id="77443-123">Do assume that if a UI works well for a finger, it also works well for a pen.</span></span> <span data-ttu-id="77443-124">讓您的應用程式可觸式變得很長，也可以提供良好的畫筆支援。</span><span class="sxs-lookup"><span data-stu-id="77443-124">Making your app touchable goes a long way to also provide good pen support.</span></span> <span data-ttu-id="77443-125">主要的差異在於手指有 blunter 提示，因此需要較大的目標。</span><span class="sxs-lookup"><span data-stu-id="77443-125">The primary difference is that fingers have a blunter tip, so they need larger targets.</span></span>

<span data-ttu-id="77443-126">有了觸控功能，您就可以直接操作物件和 UI，以提供更快速、更自然且吸引人的體驗。</span><span class="sxs-lookup"><span data-stu-id="77443-126">With touch, you can manipulate objects and UI directly, which makes for a quicker, more natural and engaging experience.</span></span>

## <a name="provide-a-great-touch-experience"></a><span data-ttu-id="77443-127">提供絕佳的觸控體驗</span><span class="sxs-lookup"><span data-stu-id="77443-127">Provide a great touch experience</span></span>

<span data-ttu-id="77443-128">您應該確保使用者可以使用觸控輸入有效率地執行重要和重要工作。</span><span class="sxs-lookup"><span data-stu-id="77443-128">You should ensure users can perform critical and important tasks efficiently using touch input.</span></span> <span data-ttu-id="77443-129">不過，特定應用程式功能（例如文字或圖元操作）可能不適合觸控，而且可以保留給最適合的輸入裝置。</span><span class="sxs-lookup"><span data-stu-id="77443-129">However, specific app functionality, like text or pixel manipulation, might not be suitable for touch and can be reserved for the most suitable input device.</span></span>

<span data-ttu-id="77443-130">如果您在開發觸控應用程式時沒有太多經驗，最好是透過進行學習。</span><span class="sxs-lookup"><span data-stu-id="77443-130">If you don't have much experience developing touch apps, it's best to learn by doing.</span></span> <span data-ttu-id="77443-131">取得具備觸控功能的電腦，將滑鼠和鍵盤放在旁邊，然後只使用您的手指與您的應用程式互動。</span><span class="sxs-lookup"><span data-stu-id="77443-131">Get a touch-enabled computer, put the mouse and keyboard aside, and use only your fingers to interact with your app.</span></span> <span data-ttu-id="77443-132">如果您有平板電腦，請嘗試將它保存在不同的位置，例如在您的膝上上、平面上的平面上，或在您的手中。</span><span class="sxs-lookup"><span data-stu-id="77443-132">If you have a tablet, experiment with holding it in different positions, such as on your lap, lying flat on a table, or in your arms while you're standing.</span></span> <span data-ttu-id="77443-133">請嘗試在直向和橫向方向使用它。</span><span class="sxs-lookup"><span data-stu-id="77443-133">Try using it in portrait and landscape orientation.</span></span>

<span data-ttu-id="77443-134">適用于觸控互動的觸控優化應用程式通常是：</span><span class="sxs-lookup"><span data-stu-id="77443-134">Touch-optimized apps that work best with touch interaction are typically:</span></span>

-   <span data-ttu-id="77443-135">**自然又直覺。**</span><span class="sxs-lookup"><span data-stu-id="77443-135">**Natural and intuitive.**</span></span> <span data-ttu-id="77443-136">互動的設計目的是要與使用者在真實世界中與物件互動的方式相對應。</span><span class="sxs-lookup"><span data-stu-id="77443-136">Interactions are designed to correspond to how users interact with objects in the real world.</span></span>
-   <span data-ttu-id="77443-137">**較不具侵入性。**</span><span class="sxs-lookup"><span data-stu-id="77443-137">**Less intrusive.**</span></span> <span data-ttu-id="77443-138">使用觸控是無訊息的，因此會比輸入或按下更少干擾。</span><span class="sxs-lookup"><span data-stu-id="77443-138">Using touch is silent, and consequently much less distracting than typing or clicking.</span></span>
-   <span data-ttu-id="77443-139">**可擕式。**</span><span class="sxs-lookup"><span data-stu-id="77443-139">**Portable.**</span></span> <span data-ttu-id="77443-140">觸控裝置更精簡，因為許多工具可在沒有鍵盤、滑鼠、畫筆或觸控板的情況下完成。</span><span class="sxs-lookup"><span data-stu-id="77443-140">Touch devices are more compact because many tasks can be completed without a keyboard, mouse, pen, or touchpad.</span></span> <span data-ttu-id="77443-141">它們也更有彈性，因為不需要工作介面。</span><span class="sxs-lookup"><span data-stu-id="77443-141">They're also more flexible because a work surface isn't required.</span></span>
-   <span data-ttu-id="77443-142">**直接且吸引人。**</span><span class="sxs-lookup"><span data-stu-id="77443-142">**Direct and engaging.**</span></span> <span data-ttu-id="77443-143">觸控讓您覺得直接操作螢幕上的物件。</span><span class="sxs-lookup"><span data-stu-id="77443-143">Touch makes you feel like you are directly manipulating objects on the screen.</span></span>
-   <span data-ttu-id="77443-144">**較不精確。**</span><span class="sxs-lookup"><span data-stu-id="77443-144">**Less accurate.**</span></span> <span data-ttu-id="77443-145">相較于滑鼠或畫筆，使用者無法正確地以觸控的方式鎖定物件。</span><span class="sxs-lookup"><span data-stu-id="77443-145">Users can't target objects as accurately with touch, compared to a mouse or pen.</span></span>

<span data-ttu-id="77443-146">觸控可提供自然的真實世界風格來進行互動。</span><span class="sxs-lookup"><span data-stu-id="77443-146">Touch provides a natural, real-world feel to interaction.</span></span> <span data-ttu-id="77443-147">直接操作和動畫藉由為物件提供逼真、動態的移動和意見反應，來完成這項印象。</span><span class="sxs-lookup"><span data-stu-id="77443-147">Direct manipulation and animation complete this impression, by giving objects a realistic, dynamic motion and feedback.</span></span> <span data-ttu-id="77443-148">例如，請考慮使用卡片遊戲。</span><span class="sxs-lookup"><span data-stu-id="77443-148">For example, consider a card game.</span></span> <span data-ttu-id="77443-149">不但方便且輕鬆地使用手指拖曳卡片，當您可以像是實體的牌一樣，也能以吸引人的真實世界感覺來滑行和旋轉卡片。</span><span class="sxs-lookup"><span data-stu-id="77443-149">Not only is it convenient and easy to drag cards using a finger, the experience takes on an engaging real-world feel when you can toss, glide, and spin the cards just like you would a physical deck.</span></span> <span data-ttu-id="77443-150">當您嘗試移動無法移動的卡片時，有更好的體驗可讓卡片受到保護，但不能防止移動，並且在釋出時就地向後復原，以清楚地指出已辨識該動作，但無法完成。</span><span class="sxs-lookup"><span data-stu-id="77443-150">And when you try to move a card that can't be moved, it's a better experience to have the card resist but not prevent movement, and settle back in place when released, to clearly indicate that the action was recognized but can't be done.</span></span>

<span data-ttu-id="77443-151">幸運的是，如果您的應用程式已經過妥善設計，提供絕佳的觸控體驗很簡單。</span><span class="sxs-lookup"><span data-stu-id="77443-151">Fortunately, if your app is already well designed, providing a great touch experience is easy to do.</span></span> <span data-ttu-id="77443-152">基於這個目的，設計完善的程式：</span><span class="sxs-lookup"><span data-stu-id="77443-152">For this purpose, a well-designed program:</span></span>

-   <span data-ttu-id="77443-153">**確保最重要的工作可以使用手指有效率地執行** (至少不涉及大量輸入或詳細圖元操作) 的工作。</span><span class="sxs-lookup"><span data-stu-id="77443-153">**Ensures most important tasks can be performed efficiently using a finger** (at least the tasks that don't involve a lot of typing or detailed pixel manipulation).</span></span>
-   <span data-ttu-id="77443-154">**使用大型控制項進行觸控。**</span><span class="sxs-lookup"><span data-stu-id="77443-154">**Uses large controls for touch.**</span></span> <span data-ttu-id="77443-155">通用控制項的最小大小為23x23 圖元 (13x13 Dlu) ，而最常使用的控制項至少是40x40 圖元 (23x22 Dlu) 。</span><span class="sxs-lookup"><span data-stu-id="77443-155">Common controls have a minimum size of 23x23 pixels (13x13 DLUs), and the most commonly used controls are at least 40x40 pixels (23x22 DLUs).</span></span> <span data-ttu-id="77443-156">為了避免沒有回應的行為，UI 元素至少應該要有5個圖元 (3 個 Dlu 之間的空格) 。</span><span class="sxs-lookup"><span data-stu-id="77443-156">To avoid unresponsive behavior, UI elements should have at least 5 pixels (3 DLUs) of space between them.</span></span> <span data-ttu-id="77443-157">針對其他控制項，請確定它們至少有一個23x23 圖元 (13x13 DLU) 按一下 [目標]，即使其靜態外觀較小也一樣。</span><span class="sxs-lookup"><span data-stu-id="77443-157">For other controls, make sure they have at least a 23x23 pixel (13x13 DLU) click target, even if their static appearance is much smaller.</span></span> <span data-ttu-id="77443-158">請參閱標準控制項大小調整。</span><span class="sxs-lookup"><span data-stu-id="77443-158">See standard control sizing.</span></span>
-   <span data-ttu-id="77443-159">**支援滑鼠輸入。**</span><span class="sxs-lookup"><span data-stu-id="77443-159">**Supports Mouse input.**</span></span> <span data-ttu-id="77443-160">互動式控制項具有明確的可見 affordances。</span><span class="sxs-lookup"><span data-stu-id="77443-160">The interactive controls have clear, visible affordances.</span></span> <span data-ttu-id="77443-161">物件具有標準滑鼠互動的標準行為 (單一和按兩下、按一下滑鼠右鍵、拖放) 。</span><span class="sxs-lookup"><span data-stu-id="77443-161">Objects have standard behaviors for the standard mouse interactions (single and double left-click, right-click, drag, and hover).</span></span>
-   <span data-ttu-id="77443-162">**支援鍵盤輸入。**</span><span class="sxs-lookup"><span data-stu-id="77443-162">**Supports keyboard input.**</span></span> <span data-ttu-id="77443-163">應用程式會提供標準的快速鍵指派，特別是針對也可以透過觸控手勢產生的導覽和編輯命令。</span><span class="sxs-lookup"><span data-stu-id="77443-163">The app provides standard shortcut key assignments, especially for navigation and editing commands that can also be generated through touch gestures.</span></span>
-   <span data-ttu-id="77443-164">**確保存取範圍。**</span><span class="sxs-lookup"><span data-stu-id="77443-164">**Ensures accessibility.**</span></span> <span data-ttu-id="77443-165">使用消費者介面自動化或 Microsoft Active Accessibility (MSAA) ，以程式設計方式存取輔助技術的 UI。</span><span class="sxs-lookup"><span data-stu-id="77443-165">Uses UI Automation or Microsoft Active Accessibility (MSAA) to provide programmatic access to the UI for assistive technologies.</span></span> <span data-ttu-id="77443-166">應用程式會適當地回應方向、主題、地區設定和系統計量變更。</span><span class="sxs-lookup"><span data-stu-id="77443-166">The app responds appropriately to orientation, theme, locale, and system metric changes.</span></span>
-   <span data-ttu-id="77443-167">**消除不必要的互動。**</span><span class="sxs-lookup"><span data-stu-id="77443-167">**Eliminates unnecessary interactions.**</span></span> <span data-ttu-id="77443-168">若要防止資料或系統存取遺失，請使用最安全且最安全的預設值。</span><span class="sxs-lookup"><span data-stu-id="77443-168">To prevent loss of data or system access, use the safest and most secure default values.</span></span> <span data-ttu-id="77443-169">如果安全性和安全性不是因素，則應用程式會選取最有可能或方便的選項。</span><span class="sxs-lookup"><span data-stu-id="77443-169">If safety and security aren't factors, the app selects the most likely or convenient option.</span></span>
-   <span data-ttu-id="77443-170">**提供暫留的對等觸控。**</span><span class="sxs-lookup"><span data-stu-id="77443-170">**Provides touch equivalent for hover.**</span></span> <span data-ttu-id="77443-171">請勿以滑鼠停留作為執行動作的唯一方法。</span><span class="sxs-lookup"><span data-stu-id="77443-171">Don't rely on hover as the only way to perform an action.</span></span>
-   <span data-ttu-id="77443-172">**確保手勢立即生效。**</span><span class="sxs-lookup"><span data-stu-id="77443-172">**Ensures gestures take effect immediately.**</span></span> <span data-ttu-id="77443-173">將連絡人點保持在使用者的手中，順暢地在筆勢中，這會將手勢對應的效果直接提供給使用者的動作。</span><span class="sxs-lookup"><span data-stu-id="77443-173">Keep contact points under the user's fingers smoothly throughout the gesture, which provides the effect of the gesture mapping directly to the user's motion.</span></span>
-   <span data-ttu-id="77443-174">**盡可能使用標準手勢。**</span><span class="sxs-lookup"><span data-stu-id="77443-174">**Uses standard gestures whenever possible.**</span></span> <span data-ttu-id="77443-175">僅適用于您的應用程式特有互動的自訂筆勢。</span><span class="sxs-lookup"><span data-stu-id="77443-175">Custom gestures only for interactions unique to your app.</span></span>
-   <span data-ttu-id="77443-176">**確保可以反轉或更正不想要或破壞性的命令。**</span><span class="sxs-lookup"><span data-stu-id="77443-176">**Ensures undesired or destructive commands can be reversed or corrected.**</span></span> <span data-ttu-id="77443-177">使用觸控時，很可能會發生意外的動作。</span><span class="sxs-lookup"><span data-stu-id="77443-177">Accidental actions are more likely when using touch.</span></span>

## <a name="guidelines-for-touch-input"></a><span data-ttu-id="77443-178">觸控輸入的指導方針</span><span class="sxs-lookup"><span data-stu-id="77443-178">Guidelines for touch input</span></span>

<span data-ttu-id="77443-179">使用觸控時，您的 Windows 應用程式可以使用實體手勢來模擬 UI 元素的直接操作。</span><span class="sxs-lookup"><span data-stu-id="77443-179">With touch, your Windows app can use physical gestures to emulate the direct manipulation of UI elements.</span></span>

<span data-ttu-id="77443-180">設計具備觸控功能的應用程式時，請考慮下列最佳做法：</span><span class="sxs-lookup"><span data-stu-id="77443-180">Consider these best practices when designing your touch-enabled app:</span></span>

<span data-ttu-id="77443-181">**回應能力對於建立直接且吸引人的觸控體驗而言是不可或缺的。**</span><span class="sxs-lookup"><span data-stu-id="77443-181">**Responsiveness is essential for creating touch experiences that feel direct and engaging.**</span></span> <span data-ttu-id="77443-182">若要直接操作，手勢必須立即生效，而物件的接觸點必須在使用者的手中順暢地停留在整個手勢中。</span><span class="sxs-lookup"><span data-stu-id="77443-182">To feel direct, gestures must take effect immediately, and an object's contact points must stay under the user's fingers smoothly throughout the gesture.</span></span> <span data-ttu-id="77443-183">觸控輸入的效果應該會直接對應到使用者的動作，因此，例如，如果使用者將手指旋轉90度，則物件也應旋轉90度。</span><span class="sxs-lookup"><span data-stu-id="77443-183">The effect of touch input should map directly to the user's motion, so, for example, if the user rotates his fingers 90 degrees, the object should rotate 90 degrees as well.</span></span> <span data-ttu-id="77443-184">任何延遲、不穩定的回應、連絡人遺失或不正確的結果，都可終結直接操作和品質的認知。</span><span class="sxs-lookup"><span data-stu-id="77443-184">Any lag, choppy response, loss of contact, or inaccurate results destroys the perception of direct manipulation and also of quality.</span></span>

<span data-ttu-id="77443-185">**一致性對於建立自然且直覺的觸控式體驗而言是不可或缺的。**</span><span class="sxs-lookup"><span data-stu-id="77443-185">**Consistency is essential for creating touch experiences that feel natural and intuitive.**</span></span> <span data-ttu-id="77443-186">當使用者學習標準手勢之後，他們會預期筆勢在所有應用程式中都具有相同的效果。</span><span class="sxs-lookup"><span data-stu-id="77443-186">Once users learn a standard gesture, they expect that gesture to have the same effect across all apps.</span></span> <span data-ttu-id="77443-187">為了避免混淆和挫折，絕對不要將非標準意義指派給標準手勢。</span><span class="sxs-lookup"><span data-stu-id="77443-187">To avoid confusion and frustration, never assign non-standard meanings to standard gestures.</span></span> <span data-ttu-id="77443-188">相反地，請使用自訂手勢進行程式的唯一互動。</span><span class="sxs-lookup"><span data-stu-id="77443-188">Instead, use custom gestures for interactions unique to your program.</span></span>

<span data-ttu-id="77443-189">接下來，我們將說明 Windows 觸控語言，但是在開始之前，請先簡短列出基本的觸控輸入詞彙。</span><span class="sxs-lookup"><span data-stu-id="77443-189">Next we'll describe the Windows touch language, but before we go on, here's a short list of basic touch input terms.</span></span>

-   <span data-ttu-id="77443-190">**手勢**</span><span class="sxs-lookup"><span data-stu-id="77443-190">**Gesture**</span></span>

    <span data-ttu-id="77443-191">手勢是在輸入裝置 (手指、手指、畫筆/手寫筆、滑鼠等) 上執行的實體 act 或動作。</span><span class="sxs-lookup"><span data-stu-id="77443-191">A gesture is the physical act or motion performed on, or by, the input device (finger, fingers, pen/stylus, mouse, and so on).</span></span> <span data-ttu-id="77443-192">例如，若要啟動、啟動或叫用命令，您可以使用單一手指點來執行觸控或觸控板裝置， (相當於滑鼠左鍵、使用畫筆來點一下，或輸入鍵盤) 。</span><span class="sxs-lookup"><span data-stu-id="77443-192">For example, to launch, activate, or invoke a command, you use a single finger tap for a touch or touchpad device (equivalent to a left-click with a mouse, a tap with a pen, or Enter on a keyboard).</span></span>

-   <span data-ttu-id="77443-193">**操作**</span><span class="sxs-lookup"><span data-stu-id="77443-193">**Manipulation**</span></span>

    <span data-ttu-id="77443-194">操作是物件或 UI 對手勢的即時反應或回應。</span><span class="sxs-lookup"><span data-stu-id="77443-194">A manipulation is the immediate, real-time reaction or response an object or UI has to a gesture.</span></span> <span data-ttu-id="77443-195">例如，投影片和滑動手勢通常會讓元素或 UI 以某種方式移動。</span><span class="sxs-lookup"><span data-stu-id="77443-195">For example, both the slide and swipe gestures typically cause an element or UI to move in some way.</span></span>

    <span data-ttu-id="77443-196">操作的最終結果、畫面上的物件和 UI 中的物件所顯示的結果是互動。</span><span class="sxs-lookup"><span data-stu-id="77443-196">The final outcome of a manipulation, how it's manifested by the object on the screen and in the UI, is the interaction.</span></span>

-   <span data-ttu-id="77443-197">**互動**</span><span class="sxs-lookup"><span data-stu-id="77443-197">**Interaction**</span></span>

    <span data-ttu-id="77443-198">互動取決於操作的解讀方式，以及操作所產生的命令或動作。</span><span class="sxs-lookup"><span data-stu-id="77443-198">Interactions depend on how a manipulation is interpreted and the command or action that results from the manipulation.</span></span> <span data-ttu-id="77443-199">例如，您可以使用投影片和滑動手勢來移動物件，但結果會因距離臨界值是否超過而有所不同。</span><span class="sxs-lookup"><span data-stu-id="77443-199">For example, objects can be moved using both the slide and swipe gestures, but the results differ depending on whether a distance threshold is crossed.</span></span> <span data-ttu-id="77443-200">您可以使用投影片來拖曳物件或平移視圖，並使用滑動來選取專案或顯示應用程式行。</span><span class="sxs-lookup"><span data-stu-id="77443-200">Slide can be used to drag an object or pan a view while swipe can be used to select an item or display an app bar.</span></span>

### <a name="the-windows-touch-language"></a><span data-ttu-id="77443-201">Windows 觸控語言</span><span class="sxs-lookup"><span data-stu-id="77443-201">The Windows touch language</span></span>

<span data-ttu-id="77443-202">Windows 提供一組精簡的觸控互動，可在整個系統中使用。</span><span class="sxs-lookup"><span data-stu-id="77443-202">Windows provides a concise set of touch interactions that are used throughout the system.</span></span> <span data-ttu-id="77443-203">以一致的方式套用這種觸控語言，可讓您的應用程式感到熟悉的使用者。</span><span class="sxs-lookup"><span data-stu-id="77443-203">Applying this touch language consistently makes your app feel familiar to what users already know.</span></span> <span data-ttu-id="77443-204">這樣可讓您的應用程式更容易學習和使用，進而提高使用者的信心。</span><span class="sxs-lookup"><span data-stu-id="77443-204">This increases user confidence by making your app easier to learn and use.</span></span> <span data-ttu-id="77443-205">若要深入瞭解觸控語言的執行，請參閱手勢、操作和互動。</span><span class="sxs-lookup"><span data-stu-id="77443-205">To learn more about touch language implementation, see Gestures, manipulations, and interactions.</span></span>

<span data-ttu-id="77443-206">**按住以學習**</span><span class="sxs-lookup"><span data-stu-id="77443-206">**Press and hold to learn**</span></span>

<span data-ttu-id="77443-207">按住滑鼠手勢會顯示詳細資訊或教學視覺效果 (例如，工具提示或操作功能表) ，而不會認可動作或命令。</span><span class="sxs-lookup"><span data-stu-id="77443-207">The press and hold gesture displays detailed info or teaching visuals (for example, a tooltip or context menu) without committing to an action or command.</span></span> <span data-ttu-id="77443-208">如果在顯示視覺效果時，會啟動滑動手勢，仍然可以移動移動。</span><span class="sxs-lookup"><span data-stu-id="77443-208">Panning is still possible if a sliding gesture is started while the visual is displayed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="77443-209">您可以在水準和垂直移動都啟用的情況下，使用按住以進行選取。</span><span class="sxs-lookup"><span data-stu-id="77443-209">You can use press and hold for selection in cases where both horizontal and vertical panning is enabled.</span></span>

 

<span data-ttu-id="77443-210">進入狀態：與畫面聯繫一或兩個手指。</span><span class="sxs-lookup"><span data-stu-id="77443-210">Entry state: One or two fingers in contact with the screen.</span></span>

<span data-ttu-id="77443-211">移動：沒有動作。</span><span class="sxs-lookup"><span data-stu-id="77443-211">Motion: No motion.</span></span>

<span data-ttu-id="77443-212">結束狀態：最後一個手指會結束手勢。</span><span class="sxs-lookup"><span data-stu-id="77443-212">Exit state: Last finger up ends the gesture.</span></span>

<span data-ttu-id="77443-213">效果：顯示詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="77443-213">Effect: Display more information.</span></span>

![\-按下 \- 以 \-learn.png](images/inter-touch-image2.png)

<span data-ttu-id="77443-215">按住滑鼠手勢。</span><span class="sxs-lookup"><span data-stu-id="77443-215">The press and hold gesture.</span></span>

<span data-ttu-id="77443-216">**暫留**</span><span class="sxs-lookup"><span data-stu-id="77443-216">**Hover**</span></span>

<span data-ttu-id="77443-217">停留是很有用的互動，因為它可讓使用者在起始動作之前，透過提示取得其他資訊。</span><span class="sxs-lookup"><span data-stu-id="77443-217">Hover is a useful interaction because it allows users to get additional information through tips before initiating an action.</span></span> <span data-ttu-id="77443-218">看到這些秘訣可讓使用者感覺更自信並減少錯誤。</span><span class="sxs-lookup"><span data-stu-id="77443-218">Seeing these tips makes users feel more confident and reduces errors.</span></span>

<span data-ttu-id="77443-219">可惜的是，觸控技術並不支援暫止，所以使用者在使用手指時無法使用滑鼠停留。</span><span class="sxs-lookup"><span data-stu-id="77443-219">Unfortunately, hover isn't supported by touch technologies, so users can't hover when using a finger.</span></span> <span data-ttu-id="77443-220">這個問題的簡單解決方法是充分利用 [暫止]，但只能以執行動作所需的方式來使用。</span><span class="sxs-lookup"><span data-stu-id="77443-220">The simple solution to this problem is to take full advantage of hover, but only in ways that are not required to perform an action.</span></span> <span data-ttu-id="77443-221">在實務上，這通常表示動作也可以藉由按一下來執行，但不一定會以完全相同的方式執行。</span><span class="sxs-lookup"><span data-stu-id="77443-221">In practice, this usually means that the action can also be performed by clicking, but not necessarily in exactly the same way.</span></span>

![顯示點擊動作範例旁邊之暫留互動範例的螢幕擷取畫面。](images/inter-touch-image13.png)

<span data-ttu-id="77443-223">在此範例中，使用者可以按一下滑鼠右鍵或按一下，以查看今天的日期。</span><span class="sxs-lookup"><span data-stu-id="77443-223">In this example, users can see today's date by either hovering or clicking.</span></span>

<span data-ttu-id="77443-224">**點擊主要動作**</span><span class="sxs-lookup"><span data-stu-id="77443-224">**Tap for primary action**</span></span>

<span data-ttu-id="77443-225">在專案上叫用其主要動作，例如啟動應用程式或執行命令。</span><span class="sxs-lookup"><span data-stu-id="77443-225">Tapping on an element invokes its primary action, for instance launching an app or executing a command.</span></span>

<span data-ttu-id="77443-226">進入狀態：一觸與螢幕或觸控板聯繫，並在按下和按住互動的時間閾值之前提起。</span><span class="sxs-lookup"><span data-stu-id="77443-226">Entry state: One finger in contact with the screen or touchpad and lifted before the time threshold for a press and hold interaction occurs.</span></span>

<span data-ttu-id="77443-227">移動：沒有動作。</span><span class="sxs-lookup"><span data-stu-id="77443-227">Motion: No motion.</span></span>

<span data-ttu-id="77443-228">結束狀態：手指結束手勢。</span><span class="sxs-lookup"><span data-stu-id="77443-228">Exit state: Finger up ends the gesture.</span></span>

<span data-ttu-id="77443-229">效果：啟動應用程式或執行命令。</span><span class="sxs-lookup"><span data-stu-id="77443-229">Effect: Launch an app or execute a command.</span></span>

![touch \- \-primary.png](images/inter-touch-image3.png)

<span data-ttu-id="77443-231">點擊手勢。</span><span class="sxs-lookup"><span data-stu-id="77443-231">The tap gesture.</span></span>

<span data-ttu-id="77443-232">**滑動至平移**</span><span class="sxs-lookup"><span data-stu-id="77443-232">**Slide to pan**</span></span>

<span data-ttu-id="77443-233">投影片主要用於移動流覽，但也可以用於移動 (，其中的平移會限制為一個方向) 、繪圖或書寫。</span><span class="sxs-lookup"><span data-stu-id="77443-233">Slide is used primarily for panning interactions but can also be used for moving (where panning is constrained to one direction), drawing, or writing.</span></span> <span data-ttu-id="77443-234">投影片也可以用來透過 (將指標滑到相關物件（例如選項按鈕) ）的方式，以較小、密集的封裝元素為目標。</span><span class="sxs-lookup"><span data-stu-id="77443-234">Slide can also be used to target small, densely packed elements by scrubbing (sliding the finger over related objects such as radio buttons).</span></span>

<span data-ttu-id="77443-235">進入狀態：與畫面聯繫一或兩個手指。</span><span class="sxs-lookup"><span data-stu-id="77443-235">Entry state: One or two fingers in contact with the screen.</span></span>

<span data-ttu-id="77443-236">移動：拖曳，以相對於彼此的相同位置與其他手指保持在相同位置。</span><span class="sxs-lookup"><span data-stu-id="77443-236">Motion: Drag, with any additional fingers remaining in same position relative to each other.</span></span>

<span data-ttu-id="77443-237">結束狀態：最後一個手指會結束手勢。</span><span class="sxs-lookup"><span data-stu-id="77443-237">Exit state: Last finger up ends the gesture.</span></span>

<span data-ttu-id="77443-238">效果：直接和緊接在手指移動時立即移動基礎物件。</span><span class="sxs-lookup"><span data-stu-id="77443-238">Effect: Move the underlying object directly and immediately as the fingers move.</span></span> <span data-ttu-id="77443-239">請務必將連絡人點保留在手勢的整個手勢中。</span><span class="sxs-lookup"><span data-stu-id="77443-239">Be sure to keep the contact point under the finger throughout the gesture.</span></span>

![觸控 \-slide.png](images/inter-touch-image4.png)

<span data-ttu-id="77443-241">平移手勢。</span><span class="sxs-lookup"><span data-stu-id="77443-241">The pan gesture.</span></span>

<span data-ttu-id="77443-242">**滑動以選取、命令和移動**</span><span class="sxs-lookup"><span data-stu-id="77443-242">**Swipe to select, command, and move**</span></span>

<span data-ttu-id="77443-243">將手指向下滑動，與移動方向的距離 (，其中平移會限制為一個方向) ，會選取清單或方格中的物件。</span><span class="sxs-lookup"><span data-stu-id="77443-243">Sliding the finger a short distance, perpendicular to the panning direction (where panning is constrained to one direction), selects objects in a list or grid.</span></span> <span data-ttu-id="77443-244">選取物件時，顯示具有相關命令的應用程式行。</span><span class="sxs-lookup"><span data-stu-id="77443-244">Display the app bar with relevant commands when objects are selected.</span></span>

<span data-ttu-id="77443-245">進入狀態：一或多個手指觸控式螢幕幕。</span><span class="sxs-lookup"><span data-stu-id="77443-245">Entry state: One or more fingers touch the screen.</span></span>

<span data-ttu-id="77443-246">移動：拖曳短距離，然後在移動互動的距離臨界值之前增益。</span><span class="sxs-lookup"><span data-stu-id="77443-246">Motion: Drag a short distance and lift before the distance threshold for a move interaction occurs.</span></span>

<span data-ttu-id="77443-247">結束狀態：最後一個手指會結束手勢。</span><span class="sxs-lookup"><span data-stu-id="77443-247">Exit state: Last finger up ends the gesture.</span></span>

<span data-ttu-id="77443-248">效果：選取、移動或移動基礎物件，或顯示應用程式行。</span><span class="sxs-lookup"><span data-stu-id="77443-248">Effect: Underlying object is selected, or moved, or app bar is displayed.</span></span> <span data-ttu-id="77443-249">請務必將連絡人點保留在手勢的整個手勢中。</span><span class="sxs-lookup"><span data-stu-id="77443-249">Be sure to keep the contact point under the finger throughout the gesture.</span></span>

![d： \\ sdkenlistment \\ m \- ux \- design \\ m \- ux \- 設計 \\ 影像 \\ 觸控 \-swipe.png](images/inter-touch-image5.png)

<span data-ttu-id="77443-251">滑動手勢。</span><span class="sxs-lookup"><span data-stu-id="77443-251">The swipe gesture.</span></span>

<span data-ttu-id="77443-252">**捏合和伸展以進行縮放**</span><span class="sxs-lookup"><span data-stu-id="77443-252">**Pinch and stretch to zoom**</span></span>

<span data-ttu-id="77443-253">縮小和延展手勢用於三種互動類型：光學縮放、調整大小和語義縮放。</span><span class="sxs-lookup"><span data-stu-id="77443-253">The pinch and stretch gestures are used for three types of interactions: optical zoom, resizing, and semantic zoom.</span></span>

<span data-ttu-id="77443-254">光學縮放會調整整個內容區域的放大層級，以取得更詳細的內容。</span><span class="sxs-lookup"><span data-stu-id="77443-254">Optical zoom adjusts the magnification level of the entire content area to get a more detailed view of the content.</span></span> <span data-ttu-id="77443-255">相反地，調整大小是一種技術，可在內容區域內調整一或多個物件的相對大小，而不需要將視圖變更為內容區域。</span><span class="sxs-lookup"><span data-stu-id="77443-255">In contrast, resizing is a technique for adjusting the relative size of one or more objects within a content area without changing the view into the content area.</span></span>

<span data-ttu-id="77443-256">「語義縮放」是一種觸控優化技術，可在單一視圖內呈現和導覽結構化資料或內容 (例如電腦的資料夾結構、檔文件庫或相片專輯) ，而不需要移動流覽、滾動或樹狀檢視控制項。</span><span class="sxs-lookup"><span data-stu-id="77443-256">Semantic zoom is a touch-optimized technique for presenting and navigating structured data or content within a single view (such as the folder structure of a computer, a library of documents, or a photo album) without the need for panning, scrolling, or tree view controls.</span></span> <span data-ttu-id="77443-257">[語義縮放] 提供兩種不同的內容，因為當您縮小時放大和縮小詳細資料時，可讓您查看更多詳細資料。</span><span class="sxs-lookup"><span data-stu-id="77443-257">Semantic zoom provides two different views of the same content by letting you see more detail as you zoom in and less detail as you zoom out.</span></span>

<span data-ttu-id="77443-258">進入狀態：兩個手指同時與螢幕連接。</span><span class="sxs-lookup"><span data-stu-id="77443-258">Entry state: Two fingers in contact with the screen at the same time.</span></span>

<span data-ttu-id="77443-259">移動：手指 (延展) 或一起 (沿著軸放大) 。</span><span class="sxs-lookup"><span data-stu-id="77443-259">Motion: Fingers move apart (stretch) or together (pinch) along an axis.</span></span>

<span data-ttu-id="77443-260">結束狀態：任何手指都會結束手勢。</span><span class="sxs-lookup"><span data-stu-id="77443-260">Exit state: Any finger up ends the gesture.</span></span>

<span data-ttu-id="77443-261">效果：直接和立即將基礎物件放大或縮小，以手指分隔或在軸上的方法。</span><span class="sxs-lookup"><span data-stu-id="77443-261">Effect: Zoom the underlying object in or out directly and immediately as the fingers separate or approach on the axis.</span></span> <span data-ttu-id="77443-262">請務必將連絡人點保留在手勢的整個手勢中。</span><span class="sxs-lookup"><span data-stu-id="77443-262">Be sure to keep the contact points under the finger throughout the gesture.</span></span>

![登陸 \-areazoom.png](images/inter-touch-image6.png)

<span data-ttu-id="77443-264">縮放手勢。</span><span class="sxs-lookup"><span data-stu-id="77443-264">The zoom gesture.</span></span>

<span data-ttu-id="77443-265">**輪流旋轉**</span><span class="sxs-lookup"><span data-stu-id="77443-265">**Turn to rotate**</span></span>

<span data-ttu-id="77443-266">以兩個或更多手指旋轉會導致物件旋轉。</span><span class="sxs-lookup"><span data-stu-id="77443-266">Rotating with two or more fingers causes an object to rotate.</span></span> <span data-ttu-id="77443-267">旋轉裝置本身即可旋轉整個螢幕。</span><span class="sxs-lookup"><span data-stu-id="77443-267">Rotate the device itself to rotate the entire screen.</span></span>

<span data-ttu-id="77443-268">進入狀態：兩個手指同時與螢幕連接。</span><span class="sxs-lookup"><span data-stu-id="77443-268">Entry state: Two fingers in contact with the screen at the same time.</span></span>

<span data-ttu-id="77443-269">移動：一或兩個手指旋轉另一個手指，並垂直移至兩者之間的線條。</span><span class="sxs-lookup"><span data-stu-id="77443-269">Motion: One or both fingers rotate around the other, moving perpendicular to the line between them.</span></span>

<span data-ttu-id="77443-270">結束狀態：任何手指都會結束手勢。</span><span class="sxs-lookup"><span data-stu-id="77443-270">Exit state: Any finger up ends the gesture.</span></span>

<span data-ttu-id="77443-271">效果：以手指旋轉的相同數量旋轉基礎物件。</span><span class="sxs-lookup"><span data-stu-id="77443-271">Effect: Rotate the underlying object the same amount as the fingers have rotated.</span></span> <span data-ttu-id="77443-272">請務必將連絡人點保留在手勢的整個手勢中。</span><span class="sxs-lookup"><span data-stu-id="77443-272">Be sure to keep the contact points under the finger throughout the gesture.</span></span>

![觸控 \-turn.png](images/inter-touch-image7.png)

<span data-ttu-id="77443-274">旋轉手勢。</span><span class="sxs-lookup"><span data-stu-id="77443-274">The rotation gesture.</span></span>

<span data-ttu-id="77443-275">只有特定物件類型的旋轉才有意義，因此它不會對應到系統 Windows 互動。</span><span class="sxs-lookup"><span data-stu-id="77443-275">Rotation makes sense only for certain types of objects, so it's not mapped to a system Windows interaction.</span></span>

<span data-ttu-id="77443-276">旋轉通常會以不同的人來完成。</span><span class="sxs-lookup"><span data-stu-id="77443-276">Rotation is often done differently by different people.</span></span> <span data-ttu-id="77443-277">有些人想要在 pivot 手指周圍旋轉一個手指，有些人想要在迴圈的動作中旋轉兩個手指。</span><span class="sxs-lookup"><span data-stu-id="77443-277">Some people prefer to rotate one finger around a pivot finger, while others prefer to rotate both fingers in a circular motion.</span></span> <span data-ttu-id="77443-278">大部分的人都使用這兩者的組合，而一個手指移動了另一個手指。</span><span class="sxs-lookup"><span data-stu-id="77443-278">Most people use a combination of the two, with one finger moving more than the other.</span></span> <span data-ttu-id="77443-279">雖然平滑旋轉到任何角度都是最佳的互動，但是在許多內容中（例如照片觀賞），最好是在使用者允許的情況下，向最接近的90度旋轉進行結算。</span><span class="sxs-lookup"><span data-stu-id="77443-279">While smooth rotation to any angle is the best interaction, in many contexts, such as photo viewing, it's best to settle to the nearest 90 degree rotation once the user lets go.</span></span> <span data-ttu-id="77443-280">在相片編輯中，您可以使用小型旋轉來將相片拉到最少。</span><span class="sxs-lookup"><span data-stu-id="77443-280">In photo editing, you can use a small rotation to straighten the photo.</span></span>

<span data-ttu-id="77443-281">**從 edge 針對應用程式命令進行滑動**</span><span class="sxs-lookup"><span data-stu-id="77443-281">**Swipe from edge for app commands**</span></span>

<span data-ttu-id="77443-282">從畫面的底部或上邊緣輕量手指，會顯示應用程式行中的應用程式命令。</span><span class="sxs-lookup"><span data-stu-id="77443-282">Swiping the finger a short distance from the bottom or top edge of the screen reveals app commands in an app bar.</span></span>

<span data-ttu-id="77443-283">進入狀態：一或多個手指接觸擋板。</span><span class="sxs-lookup"><span data-stu-id="77443-283">Entry state: One or more fingers touch the bezel.</span></span>

<span data-ttu-id="77443-284">移動：將短距離拖曳到螢幕上，然後隨即顯示。</span><span class="sxs-lookup"><span data-stu-id="77443-284">Motion: Drag a short distance onto the screen and lift.</span></span>

<span data-ttu-id="77443-285">結束狀態：最後一個手指會結束手勢。</span><span class="sxs-lookup"><span data-stu-id="77443-285">Exit state: Last finger up ends the gesture.</span></span>

<span data-ttu-id="77443-286">效果：顯示應用程式行。</span><span class="sxs-lookup"><span data-stu-id="77443-286">Effect: App bar is displayed.</span></span>

![觸控 \- 滑動 \- 底部 \-edge.png](images/inter-touch-image8.png)

![觸控式 \- 刷 \- 邊 \-edge.png](images/inter-touch-image9.png)

<span data-ttu-id="77443-289">從邊緣手勢中滑動。</span><span class="sxs-lookup"><span data-stu-id="77443-289">The swipe from edge gesture.</span></span>

<span data-ttu-id="77443-290">開發人員：如需詳細資訊，請參閱 [**DIRECTMANIPULATION \_**](/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_configuration) 設定列舉。</span><span class="sxs-lookup"><span data-stu-id="77443-290">Developers: For more info, see [**DIRECTMANIPULATION\_CONFIGURATION**](/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_configuration) enumeration.</span></span>

### <a name="control-usage"></a><span data-ttu-id="77443-291">控制使用方式</span><span class="sxs-lookup"><span data-stu-id="77443-291">Control usage</span></span>

<span data-ttu-id="77443-292">在這裡，我們會提供一些指導方針，讓您優化觸控使用的控制項。</span><span class="sxs-lookup"><span data-stu-id="77443-292">Here, we provide some guidelines for optimizing controls for touch usage.</span></span>

-   <span data-ttu-id="77443-293">**使用通用控制項。**</span><span class="sxs-lookup"><span data-stu-id="77443-293">**Use common controls.**</span></span> <span data-ttu-id="77443-294">最常見的控制項是設計來支援良好的觸控體驗。</span><span class="sxs-lookup"><span data-stu-id="77443-294">Most common controls are designed to support a good touch experience.</span></span>
-   <span data-ttu-id="77443-295">**選擇設計來支援觸控的自訂控制項。**</span><span class="sxs-lookup"><span data-stu-id="77443-295">**Choose custom controls that are designed to support touch.**</span></span> <span data-ttu-id="77443-296">您可能需要自訂控制項來支援程式的特殊體驗。</span><span class="sxs-lookup"><span data-stu-id="77443-296">You might need custom controls to support your program's special experiences.</span></span> <span data-ttu-id="77443-297">選擇自訂控制項，其：</span><span class="sxs-lookup"><span data-stu-id="77443-297">Choose custom controls that:</span></span>
    -   <span data-ttu-id="77443-298">大小可以大到足以方便進行目標和操作。</span><span class="sxs-lookup"><span data-stu-id="77443-298">Can be sized large enough to for easy targeting and manipulation.</span></span>
    -   <span data-ttu-id="77443-299">在操作時，移動和反應真實世界物件的移動和反應方式，例如有動力和摩擦。</span><span class="sxs-lookup"><span data-stu-id="77443-299">When manipulated, move and react the way real-world objects move and react, such as by having momentum and friction.</span></span>
    -   <span data-ttu-id="77443-300">的容許方式是讓使用者可以輕鬆地更正錯誤。</span><span class="sxs-lookup"><span data-stu-id="77443-300">Are forgiving by allowing users to easily correct mistakes.</span></span>
    -   <span data-ttu-id="77443-301">是誤差的容許，並按一下和拖曳。</span><span class="sxs-lookup"><span data-stu-id="77443-301">Are forgiving of inaccuracy with clicking and dragging.</span></span> <span data-ttu-id="77443-302">放在其目的地附近的物件應該會落在正確的位置。</span><span class="sxs-lookup"><span data-stu-id="77443-302">Objects that are dropped near their destination should fall into the correct place.</span></span>
    -   <span data-ttu-id="77443-303">當手指在控制項上方時，有清楚的視覺效果意見反應。</span><span class="sxs-lookup"><span data-stu-id="77443-303">Have clear visual feedback when the finger is over the control.</span></span>
-   <span data-ttu-id="77443-304">**使用受限制的控制項。**</span><span class="sxs-lookup"><span data-stu-id="77443-304">**Use constrained controls.**</span></span> <span data-ttu-id="77443-305">清單和滑杆等受限制的控制項，在設計方便觸控目標時，可以比不受限制的控制項（例如文字方塊）更好，因為它們可減少文字輸入的需要。</span><span class="sxs-lookup"><span data-stu-id="77443-305">Constrained controls like lists and sliders, when designed for easy touch targeting, can be better than unconstrained controls like text boxes because they reduce the need for text input.</span></span>
-   <span data-ttu-id="77443-306">**提供適當的預設值。**</span><span class="sxs-lookup"><span data-stu-id="77443-306">**Provide appropriate default values.**</span></span> <span data-ttu-id="77443-307">依預設，請選取最安全的 (，以防止遺失資料或系統存取) 和最安全的選項。</span><span class="sxs-lookup"><span data-stu-id="77443-307">Select the safest (to prevent loss of data or system access) and most secure option by default.</span></span> <span data-ttu-id="77443-308">如果安全性和安全性不是因素，請選取最有可能或方便的選項，以避免不必要的互動。</span><span class="sxs-lookup"><span data-stu-id="77443-308">If safety and security aren't factors, select the most likely or convenient option, thereby eliminating unnecessary interaction.</span></span>
-   <span data-ttu-id="77443-309">**提供文字自動完成。**</span><span class="sxs-lookup"><span data-stu-id="77443-309">**Provide text auto completion.**</span></span> <span data-ttu-id="77443-310">提供最可能值或最近輸入值的清單，讓文字輸入更容易。</span><span class="sxs-lookup"><span data-stu-id="77443-310">Provides a list of most likely values, or most recently input values, to make text input much easier.</span></span>
-   <span data-ttu-id="77443-311">**針對使用多重選取的重要** 工作，如果通常使用標準的多重選取清單，請提供選項來改用核取方塊清單。</span><span class="sxs-lookup"><span data-stu-id="77443-311">**For important tasks that use multiple selection**, if a standard multiple-selection list is normally used, provide an option to use a check box list instead.</span></span>

### <a name="control-sizes-and-touch-targeting"></a><span data-ttu-id="77443-312">控制項大小和觸控目標</span><span class="sxs-lookup"><span data-stu-id="77443-312">Control sizes and touch targeting</span></span>

<span data-ttu-id="77443-313">由於 fingertip 的大型介面區，太接近的小型控制項可能很難精確地鎖定目標。</span><span class="sxs-lookup"><span data-stu-id="77443-313">Due to the large surface area of the fingertip, small controls that are too close together can be difficult to target precisely.</span></span>

<span data-ttu-id="77443-314">一般而言，23x23 圖元的控制項大小 (13x13 Dlu) 是適用于任何輸入裝置的最小互動式控制項大小。</span><span class="sxs-lookup"><span data-stu-id="77443-314">As a general rule, a control size of 23x23 pixels (13x13 DLUs) is a good minimum interactive control size for any input device.</span></span> <span data-ttu-id="77443-315">相反地，15x11 圖元的微調控制項太小，無法有效使用觸控。</span><span class="sxs-lookup"><span data-stu-id="77443-315">By contrast, the spin controls at 15x11 pixels are much too small to be used effectively with touch.</span></span>

![顯示向上和向下選取按鈕的寬度和高度、測量 9 Dlu (15 圖元) 寬 x 5 Dlu (9 圖元) 高的螢幕擷取畫面。](images/inter-touch-image14.png)

<span data-ttu-id="77443-317">請記住，大小下限實際上是以實體區域為基礎，而不是圖元或 Dlu 等版面配置度量。</span><span class="sxs-lookup"><span data-stu-id="77443-317">Keep in mind that the minimum size is really based on physical area, not layout metrics such as pixels or DLUs.</span></span> <span data-ttu-id="77443-318">研究表示使用手指進行有效率、準確互動的最小目的地區域是6x6 毫米 (mm) 。</span><span class="sxs-lookup"><span data-stu-id="77443-318">Research indicates that the minimum target area for efficient, accurate interaction using a finger is 6x6 millimeters (mm).</span></span> <span data-ttu-id="77443-319">此區域會轉譯成如下的版面配置度量：</span><span class="sxs-lookup"><span data-stu-id="77443-319">This area translates to layout metrics like this:</span></span>



| <span data-ttu-id="77443-320">字型</span><span class="sxs-lookup"><span data-stu-id="77443-320">Font</span></span>             | <span data-ttu-id="77443-321">公釐</span><span class="sxs-lookup"><span data-stu-id="77443-321">Millimeters</span></span> | <span data-ttu-id="77443-322">相對圖元</span><span class="sxs-lookup"><span data-stu-id="77443-322">Relative pixels</span></span> | <span data-ttu-id="77443-323">單位</span><span class="sxs-lookup"><span data-stu-id="77443-323">DLUs</span></span>  |
|------------------|-------------|-----------------|-------|
| <span data-ttu-id="77443-324">9點 Segoe UI</span><span class="sxs-lookup"><span data-stu-id="77443-324">9 point Segoe UI</span></span> | <span data-ttu-id="77443-325">6x6</span><span class="sxs-lookup"><span data-stu-id="77443-325">6x6</span></span>         | <span data-ttu-id="77443-326">23x23</span><span class="sxs-lookup"><span data-stu-id="77443-326">23x23</span></span>           | <span data-ttu-id="77443-327">13x13</span><span class="sxs-lookup"><span data-stu-id="77443-327">13x13</span></span> |
| <span data-ttu-id="77443-328">8點 Tahoma</span><span class="sxs-lookup"><span data-stu-id="77443-328">8 point Tahoma</span></span>   | <span data-ttu-id="77443-329">6x6</span><span class="sxs-lookup"><span data-stu-id="77443-329">6x6</span></span>         | <span data-ttu-id="77443-330">23x23</span><span class="sxs-lookup"><span data-stu-id="77443-330">23x23</span></span>           | <span data-ttu-id="77443-331">15x14</span><span class="sxs-lookup"><span data-stu-id="77443-331">15x14</span></span> |



 

<span data-ttu-id="77443-332">此外，研究顯示 10x10 mm 的最小大小 (40x40 圖元) 可提供更佳的速度和正確性，也覺得更適合使用者使用。</span><span class="sxs-lookup"><span data-stu-id="77443-332">Furthermore, research shows that a minimum size of 10x10 mm (about 40x40 pixels) enables better speed and accuracy, and also feels more comfortable to users.</span></span> <span data-ttu-id="77443-333">在可行的情況下，針對最重要或常用命令所使用的命令按鈕使用此較大的大小。</span><span class="sxs-lookup"><span data-stu-id="77443-333">When practical, use this larger size for command buttons used for the most important or frequently used commands.</span></span>

<span data-ttu-id="77443-334">目標不是有巨大的控制項，只是很容易接觸觸控的控制項。</span><span class="sxs-lookup"><span data-stu-id="77443-334">The goal isn't to have giant controls, just ones that are easily used with touch.</span></span>

![顯示 Microsoft Word 工具列的螢幕擷取畫面，其中已醒目提示 [A B C 拼寫 & 文法] 按鈕，並以 41 DLU 高度和 40 DLU 寬度顯示。](images/inter-touch-image15.png)

<span data-ttu-id="77443-336">在此範例中，Microsoft Word 使用大於 10x10 mm 的按鈕來取得最重要的命令。</span><span class="sxs-lookup"><span data-stu-id="77443-336">In this example, Microsoft Word uses buttons larger than 10x10 mm for the most important commands.</span></span>

![顯示 Windows 計算機的螢幕擷取畫面。](images/inter-touch-image16.png)

<span data-ttu-id="77443-338">此版本的計算機針對其最常使用的命令使用大於 10x10 mm 的按鈕。</span><span class="sxs-lookup"><span data-stu-id="77443-338">This version of Calculator uses buttons larger than 10x10 mm for its most frequently used commands.</span></span>

<span data-ttu-id="77443-339">觸控目標沒有完美的大小。</span><span class="sxs-lookup"><span data-stu-id="77443-339">There's no perfect size for touch targets.</span></span> <span data-ttu-id="77443-340">不同的大小適用于不同的情況。</span><span class="sxs-lookup"><span data-stu-id="77443-340">Different sizes work for different situations.</span></span> <span data-ttu-id="77443-341">具有嚴重後果的動作 (例如刪除和關閉) 或經常使用的動作，都應該使用大型的觸控目標。</span><span class="sxs-lookup"><span data-stu-id="77443-341">Actions with severe consequences (such as delete and close) or frequently used actions should use large touch targets.</span></span> <span data-ttu-id="77443-342">不常使用的動作若有輕微的結果，則可以使用較小的目標。</span><span class="sxs-lookup"><span data-stu-id="77443-342">Infrequently used actions with minor consequences can use small targets.</span></span>

<span data-ttu-id="77443-343">**自訂控制項的目標大小指導方針**</span><span class="sxs-lookup"><span data-stu-id="77443-343">**Target size guidelines for custom controls**</span></span>



| <span data-ttu-id="77443-344">大小指導方針</span><span class="sxs-lookup"><span data-stu-id="77443-344">Size guideline</span></span>                                                                                 | <span data-ttu-id="77443-345">Description</span><span class="sxs-lookup"><span data-stu-id="77443-345">Description</span></span>                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![7x7 建議的最小大小](images/inter_touch_image10.jpeg)<br/>      | <span data-ttu-id="77443-347">**7x7 mm：建議的最小大小**</span><span class="sxs-lookup"><span data-stu-id="77443-347">**7x7 mm: Recommended minimum size**</span></span><br/> <span data-ttu-id="77443-348">如果觸及錯誤的目標可在一或兩個手勢中或在五秒內更正，7x7 mm 是很好的最小大小。</span><span class="sxs-lookup"><span data-stu-id="77443-348">7x7 mm is a good minimum size if touching the wrong target can be corrected in one or two gestures or within five seconds.</span></span> <span data-ttu-id="77443-349">目標之間的填補與目標大小一樣重要。</span><span class="sxs-lookup"><span data-stu-id="77443-349">Padding between targets is just as important as target size.</span></span><br/>                               |
| ![9x9 精確度的建議大小](images/inter_touch_image11.jpeg)<br/> | <span data-ttu-id="77443-351">**當精確度很重要時**</span><span class="sxs-lookup"><span data-stu-id="77443-351">**When accuracy matters**</span></span><br/> <span data-ttu-id="77443-352">具有嚴重後果的關閉、刪除和其他動作，無法承受意外的點擊。</span><span class="sxs-lookup"><span data-stu-id="77443-352">Close, delete, and other actions with severe consequences can't afford accidental taps.</span></span> <span data-ttu-id="77443-353">如果觸及錯誤的目標需要兩個以上的手勢、五秒或主要內容變更才能正確，請使用 9x9 mm 目標。</span><span class="sxs-lookup"><span data-stu-id="77443-353">Use 9x9 mm targets if touching the wrong target requires more than two gestures, five seconds, or a major context change to correct.</span></span><br/>     |
| ![5x5 大小下限](images/inter_touch_image12.jpeg)<br/>                  | <span data-ttu-id="77443-355">**當它不符合時**</span><span class="sxs-lookup"><span data-stu-id="77443-355">**When it just won't fit**</span></span><br/> <span data-ttu-id="77443-356">如果您發現自己 cramming 要符合的專案，只要觸及錯誤的目標，就可以使用一個手勢來修正。</span><span class="sxs-lookup"><span data-stu-id="77443-356">If you find yourself cramming things to fit, it's okay to use 5x5 mm targets as long as touching the wrong target can be corrected with one gesture.</span></span> <span data-ttu-id="77443-357">在此情況下，在目標之間使用 2 mm 填補非常重要。</span><span class="sxs-lookup"><span data-stu-id="77443-357">Using 2 mm of padding between targets is extremely important in this case.</span></span><br/> |



 

<span data-ttu-id="77443-358">**通用控制項的目標大小指導方針**</span><span class="sxs-lookup"><span data-stu-id="77443-358">**Target size guidelines for common controls**</span></span>

-   <span data-ttu-id="77443-359">**針對通用控制項，請使用建議的控制項大小。**</span><span class="sxs-lookup"><span data-stu-id="77443-359">**For common controls, use the recommended control sizes.**</span></span> <span data-ttu-id="77443-360">建議的控制項調整大小滿足23x23 圖元 (13x13 DLU) 最小大小，除了核取方塊和選項按鈕 (其文字寬度會稍微補償) 、微調控制項 (無法使用觸控，但卻是重複的) 和分隔器。</span><span class="sxs-lookup"><span data-stu-id="77443-360">The recommended control sizing satisfies the 23x23 pixel (13x13 DLU) minimum size, except for check boxes and radio buttons (their text width compensates somewhat), spin controls (which aren't usable with touch, but are redundant), and splitters.</span></span>

    ![顯示通用控制項範例的螢幕擷取畫面，包括音訊控制項、[立即流覽網際網路] 按鈕，以及檔案總管視窗。](images/inter-touch-image17.png)

    <span data-ttu-id="77443-362">建議的控制項大小很容易可觸式。</span><span class="sxs-lookup"><span data-stu-id="77443-362">The recommended control sizes are easily touchable.</span></span>

-   <span data-ttu-id="77443-363">**針對最重要或經常使用的命令所使用的命令按鈕，請盡可能使用40x40 圖元的最小大小 (23x22 Dlu) 。**</span><span class="sxs-lookup"><span data-stu-id="77443-363">**For command buttons used for the most important or frequently used commands, use a minimum size of 40x40 pixels (23x22 DLUs) whenever practical.**</span></span> <span data-ttu-id="77443-364">這樣做會產生更佳的速度和精確度，而且對使用者來說也更熟悉。</span><span class="sxs-lookup"><span data-stu-id="77443-364">Doing so yields better speed and accuracy, and also feels more comfortable to users.</span></span>

    ![顯示多個電子郵件 [傳送] 按鈕的螢幕擷取畫面，從左至右最小到最大的大小。](images/inter-touch-image18.png)

    <span data-ttu-id="77443-366">在實際情況下，請使用較大的命令按鈕來進行重要或常用的命令。</span><span class="sxs-lookup"><span data-stu-id="77443-366">Whenever practical, use larger command buttons for important or frequently used commands.</span></span>

-   <span data-ttu-id="77443-367">**針對其他控制項：**</span><span class="sxs-lookup"><span data-stu-id="77443-367">**For other controls:**</span></span>

    -   <span data-ttu-id="77443-368">**使用較大的點擊目標。**</span><span class="sxs-lookup"><span data-stu-id="77443-368">**Use larger click targets.**</span></span> <span data-ttu-id="77443-369">若為小型控制項，請將目標大小設為大於靜態可見的 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="77443-369">For small controls, make the target size larger than the statically visible UI element.</span></span> <span data-ttu-id="77443-370">例如，16x16 圖元圖示按鈕可以有23x23 圖元的 [目標] 按鈕，而文字元素的選取範圍會比文字和23圖元高的選取矩形8圖元。</span><span class="sxs-lookup"><span data-stu-id="77443-370">For example, 16x16 pixel icon buttons can have a 23x23 pixel click target buttons, and text elements can have selection rectangles 8 pixels wider than the text and 23 pixels high.</span></span>

        <span data-ttu-id="77443-371">正確：</span><span class="sxs-lookup"><span data-stu-id="77443-371">Correct:</span></span>

        ![顯示具有正確目標大小之工具列的螢幕擷取畫面。](images/inter-touch-image19.png)

        <span data-ttu-id="77443-373">不正確：</span><span class="sxs-lookup"><span data-stu-id="77443-373">Incorrect:</span></span>

        ![螢幕擷取畫面，顯示具有不正確大小之目的地區域的 U I 樹狀結構。](images/inter-touch-image20.png)

        <span data-ttu-id="77443-375">正確：</span><span class="sxs-lookup"><span data-stu-id="77443-375">Correct:</span></span>

        ![顯示具有正確大小之目的地區域之 U I 樹狀結構的螢幕擷取畫面。](images/inter-touch-image21.png)

        <span data-ttu-id="77443-377">在正確的範例中，按一下目標大於靜態可見的 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="77443-377">In the correct examples, the click targets are larger than the statically visible UI elements.</span></span>

    -   <span data-ttu-id="77443-378">**使用重複的按一下目標。**</span><span class="sxs-lookup"><span data-stu-id="77443-378">**Use redundant click targets.**</span></span> <span data-ttu-id="77443-379">如果控制項有重複的功能，則可接受點擊目標小於最小大小。</span><span class="sxs-lookup"><span data-stu-id="77443-379">It's acceptable for click targets to be smaller than the minimum size if that control has redundant functionality.</span></span>

        <span data-ttu-id="77443-380">例如，樹狀檢視控制項所使用的漸進式洩漏三角形僅6x9 圖元，但其功能在其相關聯的專案標籤中是多餘的。</span><span class="sxs-lookup"><span data-stu-id="77443-380">For example, the progressive disclosure triangles used by the tree view control are only 6x9 pixels, but their functionality is redundant with their associated item labels.</span></span>

        ![顯示具有重複 click 目標之 U I 樹狀結構的螢幕擷取畫面。](images/inter-touch-image22.png)

        <span data-ttu-id="77443-382">樹狀檢視三角形太小，無法輕易地可觸式，但它們在功能上有更大的相關標籤。</span><span class="sxs-lookup"><span data-stu-id="77443-382">The tree view triangles are too small to be easily touchable, but they are redundant in functionality with their larger associated labels.</span></span>

        <span data-ttu-id="77443-383">遵循系統計量。</span><span class="sxs-lookup"><span data-stu-id="77443-383">Respect system metrics.</span></span> <span data-ttu-id="77443-384">請勿將大小硬式編碼。</span><span class="sxs-lookup"><span data-stu-id="77443-384">Don't hardcode sizes.</span></span> <span data-ttu-id="77443-385">如有必要，使用者可以變更系統計量或 DPI 來滿足其需求。</span><span class="sxs-lookup"><span data-stu-id="77443-385">If necessary, users can change the system metrics or dpi to accommodate their needs.</span></span> <span data-ttu-id="77443-386">不過，將此視為最後的手段，因為使用者通常不應該調整系統設定來讓 UI 可供使用。</span><span class="sxs-lookup"><span data-stu-id="77443-386">However, treat this as a last resort because users shouldn't normally have to adjust system settings to make UI usable.</span></span>

        ![顯示左側標準功能表高度的螢幕擷取畫面，以及右邊的較大功能表高度。](images/inter-touch-image23.png)

        <span data-ttu-id="77443-388">在此範例中，功能表高度的系統度量已變更。</span><span class="sxs-lookup"><span data-stu-id="77443-388">In this example, the system metric for menu height was changed.</span></span>

<span data-ttu-id="77443-389">編輯文字</span><span class="sxs-lookup"><span data-stu-id="77443-389">Editing text</span></span>

<span data-ttu-id="77443-390">使用手指時，編輯文字是最具挑戰性的互動之一。</span><span class="sxs-lookup"><span data-stu-id="77443-390">Editing text is one of the most challenging interactions when using a finger.</span></span> <span data-ttu-id="77443-391">使用受限制的控制項、適當的預設值和自動完成功能，可以消除或減少輸入文字的需要。</span><span class="sxs-lookup"><span data-stu-id="77443-391">Using constrained controls, appropriate default values, and auto-completion eliminates or reduces the need to input text.</span></span> <span data-ttu-id="77443-392">但是，如果您的應用程式牽涉到編輯文字，您可以在使用觸控時，自動將輸入 UI 自動縮放至150%，讓使用者更具生產力。</span><span class="sxs-lookup"><span data-stu-id="77443-392">But if your app involves editing text, you can make users more productive by automatically zooming input UI up to 150 percent by default when touch is used.</span></span>

<span data-ttu-id="77443-393">例如，電子郵件程式可能會以一般可觸式大小顯示 UI，但會將輸入 UI 縮放至150% 來撰寫訊息。</span><span class="sxs-lookup"><span data-stu-id="77443-393">For example, an e-mail program could display UI at normal touchable size, but zoom the input UI to 150 percent to compose messages.</span></span>

![顯示電子郵件 U I 的螢幕擷取畫面。](images/inter-touch-image24.png)

<span data-ttu-id="77443-395">在此範例中，輸入 UI 會縮放為150%。</span><span class="sxs-lookup"><span data-stu-id="77443-395">In this example, the input UI is zoomed to 150 percent.</span></span>

### <a name="control-layout-and-spacing"></a><span data-ttu-id="77443-396">控制項版面配置和間距</span><span class="sxs-lookup"><span data-stu-id="77443-396">Control layout and spacing</span></span>

<span data-ttu-id="77443-397">控制項之間的間距是讓控制項易於可觸式的重要因素。</span><span class="sxs-lookup"><span data-stu-id="77443-397">The spacing between controls is a significant factor in making controls easily touchable.</span></span> <span data-ttu-id="77443-398">使用手指作為指標裝置時，鎖定目標會更快速但較不精確，因此使用者通常會在其預定目標以外的地方點擊。</span><span class="sxs-lookup"><span data-stu-id="77443-398">Targeting is quicker but less precise when using a finger as the pointing device, resulting in users more often tapping outside their intended target.</span></span> <span data-ttu-id="77443-399">當互動式控制項放在一起時，但實際上並不觸及時，使用者可以按一下控制項之間的非使用中空間。</span><span class="sxs-lookup"><span data-stu-id="77443-399">When interactive controls are placed very close together but are not actually touching, users may click on inactive space between the controls.</span></span> <span data-ttu-id="77443-400">因為按一下非使用中空間沒有結果或視覺效果的意見反應，所以使用者通常不確定發生什麼錯誤。</span><span class="sxs-lookup"><span data-stu-id="77443-400">Because clicking inactive space has no result or visual feedback, users are often uncertain what went wrong.</span></span>

<span data-ttu-id="77443-401">**根據所使用的輸入裝置動態調整間距。**</span><span class="sxs-lookup"><span data-stu-id="77443-401">**Dynamically adjust spacing based on the input device used.**</span></span> <span data-ttu-id="77443-402">這在暫時性的 UI （例如功能表和 flyouts）中特別有用。</span><span class="sxs-lookup"><span data-stu-id="77443-402">This is particularly useful with transient UI such as menus and flyouts.</span></span>

<span data-ttu-id="77443-403">**在互動式控制項的目的地區域之間，提供最少5圖元的 (3 Dlu) 空間。**</span><span class="sxs-lookup"><span data-stu-id="77443-403">**Provide a minimum of 5 pixels (3 DLUs) of space between the target regions of interactive controls.**</span></span> <span data-ttu-id="77443-404">如果小控制項的間距太大，則使用者需要利用精確的精確度來避免點擊錯誤的物件。</span><span class="sxs-lookup"><span data-stu-id="77443-404">If small controls are too closely spaced, the user needs to tap with precision to avoid tapping the wrong object.</span></span>

<span data-ttu-id="77443-405">**使用超過控制項之間建議的垂直間距，讓群組內的控制項更容易區分。**</span><span class="sxs-lookup"><span data-stu-id="77443-405">**Make controls within groups easier to differentiate by using more than the recommended vertical spacing between controls.**</span></span> <span data-ttu-id="77443-406">例如，在19圖元高的選項按鈕，其小於建議的最小值23圖元。</span><span class="sxs-lookup"><span data-stu-id="77443-406">For example, radio buttons at 19 pixels high are shorter than the minimum recommended size of 23 pixels.</span></span> <span data-ttu-id="77443-407">當您有可用的垂直空間時，您可以將額外4圖元的間距新增至標準7圖元，以達到與建議大小大致相同的效果。</span><span class="sxs-lookup"><span data-stu-id="77443-407">When you have vertical space available, you can achieve roughly the same effect as the recommended sizing by adding an additional 4 pixels of spacing to the standard 7 pixels.</span></span>

<span data-ttu-id="77443-408">正確：</span><span class="sxs-lookup"><span data-stu-id="77443-408">Correct:</span></span>

![顯示控制項之間垂直間距標準範例的螢幕擷取畫面。](images/inter-touch-image25.png)

<span data-ttu-id="77443-410">較佳：</span><span class="sxs-lookup"><span data-stu-id="77443-410">Better:</span></span>

![顯示有更多垂直間距的控制項範例的螢幕擷取畫面。](images/inter-touch-image26.png)

<span data-ttu-id="77443-412">在更好的範例中，選項按鈕之間的額外間距可讓您更輕鬆地區分。</span><span class="sxs-lookup"><span data-stu-id="77443-412">In the better example, the extra spacing between the radio buttons makes them easier to differentiate.</span></span>

<span data-ttu-id="77443-413">在某些情況下，使用觸控（但不是使用滑鼠或鍵盤時）時，可能會需要額外的間距。</span><span class="sxs-lookup"><span data-stu-id="77443-413">There may be situations in which extra spacing would be desirable when using touch, but not when using the mouse or keyboard.</span></span> <span data-ttu-id="77443-414">在這種情況下，只有在使用觸控來起始動作時，才使用更 spacious 的設計。</span><span class="sxs-lookup"><span data-stu-id="77443-414">In such cases, only use a more spacious design when an action is initiated using touch.</span></span>

<span data-ttu-id="77443-415">**選擇將控制項放在最可能使用之位置的版面配置。**</span><span class="sxs-lookup"><span data-stu-id="77443-415">**Choose a layout that places controls close to where they are most likely going to be used.**</span></span> <span data-ttu-id="77443-416">盡可能在社區域內保持工作互動，並找出靠近最可能使用的控制項。</span><span class="sxs-lookup"><span data-stu-id="77443-416">Keep task interactions within a small area whenever possible and locate controls close to where they are most likely going to be used.</span></span> <span data-ttu-id="77443-417">避免長距離的移動，特別是針對一般工作和拖曳。</span><span class="sxs-lookup"><span data-stu-id="77443-417">Avoid long distance hand movements, especially for common tasks and for drags.</span></span>

<span data-ttu-id="77443-418">請考慮目前的指標位置是最接近的目標，因此很容易取得。</span><span class="sxs-lookup"><span data-stu-id="77443-418">Consider that the current pointer location is the closest a target can be, making it trivial to acquire.</span></span> <span data-ttu-id="77443-419">因此，操作功能表可充分利用 Fitts 的定律，就像 Microsoft Office 使用的迷你工具列一樣。</span><span class="sxs-lookup"><span data-stu-id="77443-419">Thus, context menus take full advantage of Fitts' law, as do the mini-toolbars used by Microsoft Office.</span></span>

![顯示 Microsoft Office 並列的內容功能表和迷你工具列範例的螢幕擷取畫面。](images/inter-touch-image27.png)

<span data-ttu-id="77443-421">**避免將小型控制項放在應用程式邊緣附近或顯示。**</span><span class="sxs-lookup"><span data-stu-id="77443-421">**Avoid placing small controls near the edge of the app or the display.**</span></span> <span data-ttu-id="77443-422">接近邊緣的小型目標可能很難接觸 (顯示 bezels 可能會干擾邊緣手勢) 。</span><span class="sxs-lookup"><span data-stu-id="77443-422">Small targets near edges can be difficult to touch (display bezels can interfere with edge gestures).</span></span> <span data-ttu-id="77443-423">為了確保控制項在視窗最大化時可以輕鬆地設為目標，請將其設為至少23x23 圖元 (13x13 Dlu) 或將它們放在視窗邊緣以外。</span><span class="sxs-lookup"><span data-stu-id="77443-423">To ensure that controls are easy to target when a window is maximized, either make them at least 23x23 pixels (13x13 DLUs) or place them away from the window edge.</span></span>

<span data-ttu-id="77443-424">**使用建議的間距。**</span><span class="sxs-lookup"><span data-stu-id="77443-424">**Use the recommended spacing.**</span></span> <span data-ttu-id="77443-425">建議的間距適合觸控。</span><span class="sxs-lookup"><span data-stu-id="77443-425">The recommended spacing is touch-friendly.</span></span> <span data-ttu-id="77443-426">不過，如果您的應用程式可受益于較大的大小和間距，請考慮建議的大小調整，並在適當時調整間距。</span><span class="sxs-lookup"><span data-stu-id="77443-426">However, if your app can benefit from larger sizing and spacing, consider the recommended sizing and spacing to be minimums when appropriate.</span></span>

<span data-ttu-id="77443-427">**在互動式控制項之間提供至少5個圖元 (三個 Dlu) 空間。**</span><span class="sxs-lookup"><span data-stu-id="77443-427">**Provide at least 5 pixels (3 DLUs) of space between interactive controls.**</span></span> <span data-ttu-id="77443-428">這樣做可避免使用者在想要的目標之外時，產生混淆。</span><span class="sxs-lookup"><span data-stu-id="77443-428">Doing so prevents confusion when users tap outside their intended target.</span></span>

<span data-ttu-id="77443-429">請考慮在控制項群組（例如命令連結、核取方塊和選項按鈕，以及群組之間）新增超過建議的垂直間距。</span><span class="sxs-lookup"><span data-stu-id="77443-429">Consider adding more than the recommended vertical spacing within groups of controls, such as command links, check boxes, and radio buttons, as well as between the groups.</span></span> <span data-ttu-id="77443-430">這麼做可讓您更輕鬆地區分。</span><span class="sxs-lookup"><span data-stu-id="77443-430">Doing so makes them easier to differentiate.</span></span>

<span data-ttu-id="77443-431">**當使用觸控來起始動作時，請考慮以動態方式新增超過建議的垂直間距。**</span><span class="sxs-lookup"><span data-stu-id="77443-431">**Consider adding more than the recommended vertical spacing dynamically when an action is initiated using touch.**</span></span> <span data-ttu-id="77443-432">這麼做可讓物件更容易區分，但在使用鍵盤或滑鼠時，不會佔用更多空間。</span><span class="sxs-lookup"><span data-stu-id="77443-432">Doing so makes objects easier to differentiate, but without taking more space when using a keyboard or mouse.</span></span> <span data-ttu-id="77443-433">將間距增加為其正常大小的第三個，或至少8個圖元。</span><span class="sxs-lookup"><span data-stu-id="77443-433">Increase the spacing by a third of its normal size or at least 8 pixels.</span></span>

![image](images/inter-touch-image28.png)

<span data-ttu-id="77443-435">在此範例中，使用觸控顯示時，Windows 7 工作列跳躍清單會更 spacious。</span><span class="sxs-lookup"><span data-stu-id="77443-435">In this example, Windows 7 taskbar Jump Lists are more spacious when displayed using touch.</span></span>

### <a name="interaction"></a><span data-ttu-id="77443-436">互動</span><span class="sxs-lookup"><span data-stu-id="77443-436">Interaction</span></span>

<span data-ttu-id="77443-437">使用正確的控制項可讓您只是觸控優化應用程式的一部分，您也必須考慮這些控制項支援的整體互動模型。</span><span class="sxs-lookup"><span data-stu-id="77443-437">Using the correct controls gets you only part of the way to a touch-optimized app, you also need to consider the overall interaction model those controls support.</span></span> <span data-ttu-id="77443-438">以下是一些指導方針，可協助您進行此工作。</span><span class="sxs-lookup"><span data-stu-id="77443-438">Here are a few guidelines to help you with this.</span></span>

-   <span data-ttu-id="77443-439">**將滑鼠暫留為多餘。**</span><span class="sxs-lookup"><span data-stu-id="77443-439">**Make hover redundant.**</span></span> <span data-ttu-id="77443-440">大部分的觸控技術都不支援暫止，所以具有這類 touchscreens 的使用者無法執行任何需要停留的工作。</span><span class="sxs-lookup"><span data-stu-id="77443-440">Hover isn't supported by most touch technologies, so users with such touchscreens can't perform any tasks that require hovering.</span></span>
-   <span data-ttu-id="77443-441">**對於需要文字輸入的應用程式，請透過下列方式將觸控鍵盤功能完全整合** ：</span><span class="sxs-lookup"><span data-stu-id="77443-441">**For apps that need text input, fully integrate the touch keyboard feature** by:</span></span>
    -   <span data-ttu-id="77443-442">為使用者輸入提供適當的預設值。</span><span class="sxs-lookup"><span data-stu-id="77443-442">Providing appropriate default values for user input.</span></span>
    -   <span data-ttu-id="77443-443">適當時提供自動完成的建議。</span><span class="sxs-lookup"><span data-stu-id="77443-443">Providing auto-complete suggestions when appropriate.</span></span>

    > [!Note]  
    > <span data-ttu-id="77443-444">開發人員：如需有關整合觸控鍵盤的詳細資訊，請參閱 [**ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel)。</span><span class="sxs-lookup"><span data-stu-id="77443-444">Developers: For more info about integrating the touch keyboard, see [**ITextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel).</span></span>

     

-   <span data-ttu-id="77443-445">**如果您的程式有需要編輯文字的工作，可讓使用者縮放內容 UI。**</span><span class="sxs-lookup"><span data-stu-id="77443-445">**Allow users to zoom the content UI if your program has tasks that require editing text.**</span></span> <span data-ttu-id="77443-446">使用觸控時，請考慮自動縮放至150%。</span><span class="sxs-lookup"><span data-stu-id="77443-446">Consider automatically zooming to 150 percent when touch is used.</span></span>
-   <span data-ttu-id="77443-447">**在適當的情況下提供順暢、回應式的移動和縮放。**</span><span class="sxs-lookup"><span data-stu-id="77443-447">**Provide smooth, responsive panning and zooming wherever appropriate.**</span></span> <span data-ttu-id="77443-448">在平移或縮放之後快速重繪，以保持回應。</span><span class="sxs-lookup"><span data-stu-id="77443-448">Redraw quickly after a pan or zoom to remain responsive.</span></span> <span data-ttu-id="77443-449">這麼做是為了讓直接操作感覺成為真正的直接操作所需。</span><span class="sxs-lookup"><span data-stu-id="77443-449">Doing so is necessary to make direct manipulation feel truly direct.</span></span>
-   <span data-ttu-id="77443-450">**在移動流覽或縮放期間，請確定連絡人點在筆勢中保持在手指下。**</span><span class="sxs-lookup"><span data-stu-id="77443-450">**During a pan or zoom, make sure that the contact points stay under the finger throughout the gesture.**</span></span> <span data-ttu-id="77443-451">否則，就難以控制平移或縮放。</span><span class="sxs-lookup"><span data-stu-id="77443-451">Otherwise, the pan or zoom is difficult to control.</span></span>
-   <span data-ttu-id="77443-452">**因為手勢是記下的，所以請在應用程式之間指派一致的意義。**</span><span class="sxs-lookup"><span data-stu-id="77443-452">**Because gestures are memorized, assign them meanings that are consistent across apps.**</span></span> <span data-ttu-id="77443-453">請勿對具有固定語義的手勢提供不同意義。</span><span class="sxs-lookup"><span data-stu-id="77443-453">Don't give different meanings to gestures with fixed semantics.</span></span> <span data-ttu-id="77443-454">請改用適當的應用程式特定手勢。</span><span class="sxs-lookup"><span data-stu-id="77443-454">Use an appropriate app-specific gesture instead.</span></span>

### <a name="forgiveness"></a><span data-ttu-id="77443-455">寬恕</span><span class="sxs-lookup"><span data-stu-id="77443-455">Forgiveness</span></span>

<span data-ttu-id="77443-456">直接操作可讓觸控自然、具表達性、有效率且吸引人。</span><span class="sxs-lookup"><span data-stu-id="77443-456">Direct manipulation makes touch natural, expressive, efficient, and engaging.</span></span> <span data-ttu-id="77443-457">不過，在有直接操作的情況下，可能會有意外的操作，因此需要容許。</span><span class="sxs-lookup"><span data-stu-id="77443-457">However, where there is direct manipulation, there can be accidental manipulation and therefore the need for forgiveness.</span></span>

<span data-ttu-id="77443-458">容許可讓您輕鬆地反向或更正不想要的動作。</span><span class="sxs-lookup"><span data-stu-id="77443-458">Forgiveness is the ability to reverse or correct an undesired action easily.</span></span> <span data-ttu-id="77443-459">您可以藉由提供復原、提供良好的視覺反應、在常用的命令與破壞性命令之間進行清楚的實體分隔，讓使用者輕鬆地更正錯誤，來容許觸控體驗。</span><span class="sxs-lookup"><span data-stu-id="77443-459">You make a touch experience forgiving by providing undo, giving good visual feedback, having a clear physical separation between frequently used commands and destructive commands, and allowing users to correct mistakes easily.</span></span> <span data-ttu-id="77443-460">與容許相關聯，會防止在一開始發生不想要的動作，您可以使用限制的控制項，並確認具有非預期結果的具風險動作或命令。</span><span class="sxs-lookup"><span data-stu-id="77443-460">Associated with forgiveness is preventing undesired actions from happening in the first place, which you can do by using constrained controls and confirmations for risky actions or commands that have unintended consequences.</span></span>

-   <span data-ttu-id="77443-461">**提供復原命令。**</span><span class="sxs-lookup"><span data-stu-id="77443-461">**Provide an Undo command.**</span></span> <span data-ttu-id="77443-462">最好提供簡單的方法來復原所有命令，但您的應用程式可能會有一些無法復原其效果的命令。</span><span class="sxs-lookup"><span data-stu-id="77443-462">It's best to provide a simple way to undo all commands, but your app may have some commands whose effect cannot be undone.</span></span>
-   <span data-ttu-id="77443-463">**只要可行，請在手指下提供良好的意見反應，但不要採取動作，直到跟上為止。**</span><span class="sxs-lookup"><span data-stu-id="77443-463">**Whenever practical, provide good feedback on finger down, but don't take actions until finger up.**</span></span> <span data-ttu-id="77443-464">這麼做可讓使用者在他們進行之前更正錯誤。</span><span class="sxs-lookup"><span data-stu-id="77443-464">Doing so allows users to correct mistakes before they make them.</span></span>
-   <span data-ttu-id="77443-465">**只要可行，就能讓使用者輕鬆地更正錯誤。**</span><span class="sxs-lookup"><span data-stu-id="77443-465">**Whenever practical, allow users to correct mistakes easily.**</span></span> <span data-ttu-id="77443-466">如果動作會在手指上生效，可讓使用者在手指仍關閉時滑動，以修正錯誤。</span><span class="sxs-lookup"><span data-stu-id="77443-466">If an action takes effect on finger up, allow users to correct mistakes by sliding while the finger is still down.</span></span>
-   <span data-ttu-id="77443-467">**在實際情況下，表示 resisting 移動時無法執行直接操作。**</span><span class="sxs-lookup"><span data-stu-id="77443-467">**Whenever practical, indicate that a direct manipulation can't be performed by resisting the movement.**</span></span> <span data-ttu-id="77443-468">允許進行移動，但在釋出時，物件會就地向後復原，以明確指出已辨識該動作，但無法完成。</span><span class="sxs-lookup"><span data-stu-id="77443-468">Allow the movement to happen, but have the object settle back in place when released to clearly indicate the action was recognized but can't be done.</span></span>
-   <span data-ttu-id="77443-469">**在經常使用的命令和破壞性命令之間有清楚的實體分隔。**</span><span class="sxs-lookup"><span data-stu-id="77443-469">**Have clear physical separation between frequently used commands and destructive commands.**</span></span> <span data-ttu-id="77443-470">否則，使用者可能不小心接觸到破壞性命令。</span><span class="sxs-lookup"><span data-stu-id="77443-470">Otherwise, users might touch destructive commands accidentally.</span></span> <span data-ttu-id="77443-471">如果命令的效果很大，而且無法輕易復原或效果無法立即察覺，則會將其視為具破壞性的命令。</span><span class="sxs-lookup"><span data-stu-id="77443-471">A command is considered destructive if its effect is widespread and either it cannot be easily undone or the effect isn't immediately noticeable.</span></span>
-   <span data-ttu-id="77443-472">**確認具有非預期結果的具風險動作或命令的命令。**</span><span class="sxs-lookup"><span data-stu-id="77443-472">**Confirm commands for risky actions or commands that have unintended consequences.**</span></span> <span data-ttu-id="77443-473">基於此目的，請使用確認對話方塊。</span><span class="sxs-lookup"><span data-stu-id="77443-473">Use a confirmation dialog box for this purpose.</span></span>
-   <span data-ttu-id="77443-474">**請考慮確認使用者在使用觸控時可能會不小心執行的任何其他動作，而這可能會忽略或難以復原。**</span><span class="sxs-lookup"><span data-stu-id="77443-474">**Consider confirming any other actions that users tend to do accidentally when using touch, and which either go unnoticed or are difficult to undo.**</span></span> <span data-ttu-id="77443-475">一般來說，這些稱為「例行確認」，建議您根據使用者不常使用滑鼠或鍵盤來發出這類命令的假設。</span><span class="sxs-lookup"><span data-stu-id="77443-475">Normally, these are called routine confirmations and are discouraged based on the assumption that users don't often issue such commands by accident with a mouse or keyboard.</span></span> <span data-ttu-id="77443-476">若要避免不必要的確認，請只在使用觸控來起始命令時才顯示這些確認。</span><span class="sxs-lookup"><span data-stu-id="77443-476">To prevent unnecessary confirmations, present these confirmations only if the command was initiated using touch.</span></span>

    <span data-ttu-id="77443-477">使用者通常會不小心使用觸控的互動，可以接受例行確認。</span><span class="sxs-lookup"><span data-stu-id="77443-477">Routine confirmations are acceptable for interactions that users often do accidentally using touch.</span></span>

    <span data-ttu-id="77443-478">開發人員：您可以使用 [**輸入 \_ 訊息 \_ 來源**](/windows/win32/api/winuser/ns-winuser-input_message_source) API 來區分滑鼠事件和觸控事件。</span><span class="sxs-lookup"><span data-stu-id="77443-478">Developers: You can distinguish between mouse events and touch events using the [**INPUT\_MESSAGE\_SOURCE**](/windows/win32/api/winuser/ns-winuser-input_message_source) API.</span></span>

