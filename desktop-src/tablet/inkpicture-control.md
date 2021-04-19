---
description: Tablet PC InkPicture 控制項的參考主題。
ms.assetid: 1ced9779-dae5-4f9a-8a68-b2c0d041d5b4
title: InkPicture 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded5295d48e4bb14b3c0d83713f33939a360cff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985059"
---
# <a name="inkpicture-control"></a><span data-ttu-id="f4fec-103">InkPicture 控制項</span><span class="sxs-lookup"><span data-stu-id="f4fec-103">InkPicture Control</span></span>

<span data-ttu-id="f4fec-104">[InkPicture](inkpicture-control-reference.md)控制項可讓您將影像 ( .jpg、.bmp、.png 或 .gif 格式) 在使用者可以加入筆墨的應用程式中。</span><span class="sxs-lookup"><span data-stu-id="f4fec-104">The [InkPicture](inkpicture-control-reference.md) control enables you to place an image (.jpg, .bmp, .png, or .gif format) in an application that users can add ink to.</span></span> <span data-ttu-id="f4fec-105">它適用于不需要將筆墨辨識為文字，但會儲存為筆墨的情況。</span><span class="sxs-lookup"><span data-stu-id="f4fec-105">It is intended for scenarios in which ink need not be recognized as text but is stored as ink.</span></span>

<span data-ttu-id="f4fec-106">使用者使用畫筆將筆墨新增至透明層。</span><span class="sxs-lookup"><span data-stu-id="f4fec-106">Users add ink to a transparent layer using a pen.</span></span> <span data-ttu-id="f4fec-107">使用者可以重新調整 [InkPicture](inkpicture-control-reference.md) 視窗的大小，而不會遺失任何筆墨資訊，即使在調整大小的情況下裁剪筆墨也一樣。</span><span class="sxs-lookup"><span data-stu-id="f4fec-107">Users can re-size an [InkPicture](inkpicture-control-reference.md) window without losing any ink information, even if the ink is cropped when re-sizing.</span></span>

<span data-ttu-id="f4fec-108">[InkPicture](inkpicture-control-reference.md)控制項包含基本列印支援;不過，您可以自行執行預覽列印或其他先進的列印功能。</span><span class="sxs-lookup"><span data-stu-id="f4fec-108">The [InkPicture](inkpicture-control-reference.md) control includes basic printing support; however, it is up to you to implement print preview or other advanced printing capabilities.</span></span>

<span data-ttu-id="f4fec-109">Managed ( .NET Framework [InkPicture](/previous-versions/ms583740(v=vs.100)) 的) 執行會繼承 [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) 類別。</span><span class="sxs-lookup"><span data-stu-id="f4fec-109">The managed (.NET Framework) implementation of [InkPicture](/previous-versions/ms583740(v=vs.100)) inherits from the [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) class.</span></span>

<span data-ttu-id="f4fec-110">依預設，如果不在高對比模式中，則筆墨會著色為黑色;否則，它會設定為目前的系統色彩設定 (色彩 \_ WINDOWTEXT) 值。</span><span class="sxs-lookup"><span data-stu-id="f4fec-110">By default, ink is colored black if not in high-contrast mode; otherwise, it is set to the current system color setting (COLOR\_WINDOWTEXT) value.</span></span> <span data-ttu-id="f4fec-111">此外，根據預設， [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) 是 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="f4fec-111">Also, by default [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) is **FALSE**.</span></span>

<span data-ttu-id="f4fec-112">在 [InkPicture](inkpicture-control-reference.md) 控制項中，使用 [**筆墨**](inkdisp-class.md) 物件來載入及儲存筆跡。</span><span class="sxs-lookup"><span data-stu-id="f4fec-112">Within the [InkPicture](inkpicture-control-reference.md) control, use the [**Ink**](inkdisp-class.md) object to load and save ink.</span></span>

> [!Note]  
> <span data-ttu-id="f4fec-113">當您將 [**system.windows.controls.inkcanvas.editingmode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) 設定為 [ **刪除** ] 或 [ **選取**] 時，就會觸發其他事件 (例如 [**筆觸**](inkpicture-stroke.md) 事件) 。</span><span class="sxs-lookup"><span data-stu-id="f4fec-113">When you set the [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) to **Delete** or **Select**, other events (such as the [**Stroke**](inkpicture-stroke.md) event) are triggered.</span></span> <span data-ttu-id="f4fec-114">如果您想要執行自己的刪除或選取模式，這些事件會很有用。</span><span class="sxs-lookup"><span data-stu-id="f4fec-114">These events are useful if you want to implement your own delete or select modes.</span></span>

 

<span data-ttu-id="f4fec-115">如需 [InkPicture](inkpicture-control-reference.md) 控制項的詳細參考資訊，請參閱 InkPicture。</span><span class="sxs-lookup"><span data-stu-id="f4fec-115">For detailed reference information about the [InkPicture](inkpicture-control-reference.md) control, see InkPicture.</span></span>

<span data-ttu-id="f4fec-116">下列各節詳細說明 [InkPicture](inkpicture-control-reference.md) 控制項的使用：</span><span class="sxs-lookup"><span data-stu-id="f4fec-116">The following sections detail the use of the [InkPicture](inkpicture-control-reference.md) control:</span></span>

-   [<span data-ttu-id="f4fec-117">使用圖片</span><span class="sxs-lookup"><span data-stu-id="f4fec-117">Working with Pictures</span></span>](working-with-pictures.md)
-   [<span data-ttu-id="f4fec-118">在舊版 Windows 上使用 InkPicture</span><span class="sxs-lookup"><span data-stu-id="f4fec-118">Using InkPicture on Earlier Versions of Windows</span></span>](using-inkpicture-on-earlier-versions-of-windows.md)

 

 
