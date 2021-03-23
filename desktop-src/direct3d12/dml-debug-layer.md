---
title: 使用 DirectML debug layer
description: DirectML debug layer 是選擇性的開發階段元件，可協助您進行 DirectML 程式碼的偵錯工具。
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: f885595e5cc3b3890d208875fb92e47e0dc5e337
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "104548397"
---
# <a name="using-the-directml-debug-layer"></a><span data-ttu-id="e8d08-103">使用 DirectML debug layer</span><span class="sxs-lookup"><span data-stu-id="e8d08-103">Using the DirectML debug layer</span></span>

<span data-ttu-id="e8d08-104">DirectML debug layer 是選擇性的開發階段元件，可協助您進行 DirectML 程式碼的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="e8d08-104">The DirectML debug layer is an optional development-time component that helps you in debugging your DirectML code.</span></span> <span data-ttu-id="e8d08-105">Debug 層是個別圖形工具套件的一部分，以隨 [選](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (FOD) 的形式散發。</span><span class="sxs-lookup"><span data-stu-id="e8d08-105">The debug layer is part of a separate Graphics Tools package, distributed as a [Feature-on-Demand](/windows-hardware/manufacture/desktop/features-on-demand-v2--capabilities) (FOD).</span></span> <span data-ttu-id="e8d08-106">您必須在系統上安裝圖形工具 FOD，才能使用 debug 圖層。</span><span class="sxs-lookup"><span data-stu-id="e8d08-106">The Graphics Tools FOD must be installed on your system in order to use the debug layer.</span></span>

<span data-ttu-id="e8d08-107">強烈建議您在使用 DirectML 開發應用程式時啟用 debug 層，因為它可以在 API 使用方式不正確時提供寶貴的資訊。</span><span class="sxs-lookup"><span data-stu-id="e8d08-107">We highly recommended that you enable the debug layer while developing applications using DirectML, because it can provide invaluable information in the event of invalid API usage.</span></span>

## <a name="installing-the-directml-debug-layer"></a><span data-ttu-id="e8d08-108">安裝 DirectML debug layer</span><span class="sxs-lookup"><span data-stu-id="e8d08-108">Installing the DirectML debug layer</span></span>

<span data-ttu-id="e8d08-109">若要視需要安裝選擇性的圖形工具功能 (FOD) 封裝，請從系統管理員 Powershell 提示字元執行下列命令。</span><span class="sxs-lookup"><span data-stu-id="e8d08-109">To install the optional Graphics Tools feature-on-demand (FOD) package, run the following command from an administrator Powershell prompt.</span></span>

```powershell
Add-WindowsCapability -Online -Name "Tools.Graphics.DirectX~~~~0.0.1.0"
```

<span data-ttu-id="e8d08-110">或者，您也可以從 Windows 10 設定中安裝圖形工具套件。</span><span class="sxs-lookup"><span data-stu-id="e8d08-110">Alternatively, you can install the Graphics Tools package from within Windows 10 Settings.</span></span> <span data-ttu-id="e8d08-111">流覽至 [**設定**  >  **應用**  >  **程式] & 功能**  >  **選擇性功能**  >  **的 [新增功能**> 然後選取 [**圖形工具**]。</span><span class="sxs-lookup"><span data-stu-id="e8d08-111">Navigate to **Settings** > **Apps** > **Apps & features** > **Optional features** > **Add a feature** > then select **Graphics Tools**.</span></span>

## <a name="enabling-the-directml-debug-layer"></a><span data-ttu-id="e8d08-112">啟用 DirectML debug layer</span><span class="sxs-lookup"><span data-stu-id="e8d08-112">Enabling the DirectML debug layer</span></span>

<span data-ttu-id="e8d08-113">安裝圖形工具套件之後，您可以在呼叫 [**DMLCreateDevice**](/windows/win32/api/directml/nf-directml-dmlcreatedevice)時提供 [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) ，以啟用 DirectML 的調試層。</span><span class="sxs-lookup"><span data-stu-id="e8d08-113">Once the Graphics Tools package is installed, you can enable the DirectML debug layer by supplying  [**DML_CREATE_DEVICE_FLAG_DEBUG**](/windows/win32/api/directml/ne-directml-dml_create_device_flags) when you call [**DMLCreateDevice**](/windows/win32/api/directml/nf-directml-dmlcreatedevice).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e8d08-114">您必須先啟用 Direct3D 12 debug 層。</span><span class="sxs-lookup"><span data-stu-id="e8d08-114">You must first enable the Direct3D 12 debug layer.</span></span> <span data-ttu-id="e8d08-115">然後藉由呼叫 \**DMLCreateDevice\*\*\*來啟用 DirectML* debug layer。</span><span class="sxs-lookup"><span data-stu-id="e8d08-115">And *then* enable the DirectML debug layer by calling **DMLCreateDevice**.</span></span>

<span data-ttu-id="e8d08-116">一旦您啟用了 DirectML debug 圖層，任何 DirectML 錯誤或不正確 API 呼叫都會導致以 debug 輸出的形式發出調試資訊。</span><span class="sxs-lookup"><span data-stu-id="e8d08-116">Once you've enabled the DirectML debug layer, any DirectML errors or invalid API calls will cause debugging information to be emitted as debug output.</span></span> <span data-ttu-id="e8d08-117">以下為範例。</span><span class="sxs-lookup"><span data-stu-id="e8d08-117">Here's an example.</span></span>

```console
DML_OPERATOR_CONVOLUTION: invalid D3D12_HEAP_TYPE. DirectML requires all bound buffers to be D3D12_HEAP_TYPE_DEFAULT.
```

## <a name="see-also"></a><span data-ttu-id="e8d08-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8d08-118">See also</span></span>

* [<span data-ttu-id="e8d08-119">DMLCreateDevice 函式</span><span class="sxs-lookup"><span data-stu-id="e8d08-119">DMLCreateDevice function</span></span>](/windows/win32/api/directml/nf-directml-dmlcreatedevice)
* [<span data-ttu-id="e8d08-120">可用的功能-隨選</span><span class="sxs-lookup"><span data-stu-id="e8d08-120">Available Features-on-Demand</span></span>](/windows-hardware/manufacture/desktop/features-on-demand-non-language-fod)
* [<span data-ttu-id="e8d08-121">使用以 GPU 為基礎的驗證與 Direct3D 12 Debug Layer</span><span class="sxs-lookup"><span data-stu-id="e8d08-121">Use GPU-based validation with the Direct3D 12 Debug Layer</span></span>](/windows/desktop/direct3d12/using-d3d12-debug-layer-gpu-based-validation)
* [<span data-ttu-id="e8d08-122">Direct3D 12 Debug Layer 參考</span><span class="sxs-lookup"><span data-stu-id="e8d08-122">Direct3D 12 Debug Layer reference</span></span>](/windows/desktop/direct3d12/direct3d-12-sdklayers-reference)
