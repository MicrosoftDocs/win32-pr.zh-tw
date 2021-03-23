---
title: 處理 DirectML 中的錯誤和裝置移除
description: 本主題討論如何將 DirectML 裝置移除和其他錯誤情況進行調試。
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: b4567558b8b75685db16796e921f3daf35b849a1
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548396"
---
# <a name="handling-errors-and-device-removal-in-directml"></a><span data-ttu-id="81e19-103">處理 DirectML 中的錯誤和裝置移除</span><span class="sxs-lookup"><span data-stu-id="81e19-103">Handling errors and device-removal in DirectML</span></span>

## <a name="device-removal"></a><span data-ttu-id="81e19-104">裝置-移除</span><span class="sxs-lookup"><span data-stu-id="81e19-104">Device-removal</span></span>

<span data-ttu-id="81e19-105">如果發生無法復原的錯誤，DirectML 裝置可能會進入「裝置已移除」狀態。</span><span class="sxs-lookup"><span data-stu-id="81e19-105">If an unrecoverable error occurs, the DirectML device may enter a "device-removed" state.</span></span> <span data-ttu-id="81e19-106">導致裝置移除的無法復原錯誤包括不正確 API 使用方式 (針對未傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)) 、驅動程式錯誤、硬體錯誤或記憶體不足 (OOM) 條件的方法。</span><span class="sxs-lookup"><span data-stu-id="81e19-106">Unrecoverable errors that cause device-removal include invalid API usage (for methods that don't return an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)), driver error, hardware fault, or out-of-memory (OOM) conditions.</span></span>

<span data-ttu-id="81e19-107">移除 DirectML 裝置時，裝置上的所有方法呼叫，以及該裝置所建立的每個物件都不會成為任何 ops。</span><span class="sxs-lookup"><span data-stu-id="81e19-107">When a DirectML device is removed, all method calls on the device, and every object created by that device, become no-ops.</span></span> <span data-ttu-id="81e19-108">如果是傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)的方法，則會傳回 [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/direct3ddxgi/dxgi-error) 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="81e19-108">For methods that return an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes), a [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/direct3ddxgi/dxgi-error) error code is returned.</span></span> <span data-ttu-id="81e19-109">您可以使用 [ **IDMLDevice：： GetDeviceRemovedReason** 方法](/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason)來檢查 DirectML 裝置是否已移除，並取得更詳細的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="81e19-109">You can use the [**IDMLDevice::GetDeviceRemovedReason** method](/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason) to check whether the DirectML device has been removed, and to retrieve a more detailed error code.</span></span>

<span data-ttu-id="81e19-110">除了釋出受影響的裝置及其所有子系，然後從頭重新建立 DirectML 裝置以外，您無法從裝置移除復原。</span><span class="sxs-lookup"><span data-stu-id="81e19-110">You can't recover from device-removal except by releasing the affected device and all its children, then re-creating the DirectML device from scratch.</span></span>

<span data-ttu-id="81e19-111">裝置移除基礎 Direct3D 12 裝置也會使 DirectML 裝置被移除。</span><span class="sxs-lookup"><span data-stu-id="81e19-111">Device-removal of the underlying Direct3D 12 device also causes the DirectML device to be removed.</span></span> <span data-ttu-id="81e19-112">不過，反向操作則不可行。</span><span class="sxs-lookup"><span data-stu-id="81e19-112">However, the reverse is not true.</span></span> <span data-ttu-id="81e19-113">DirectML 裝置移除可能不一定會導致基礎 Direct3D 12 裝置被移除。</span><span class="sxs-lookup"><span data-stu-id="81e19-113">DirectML device-removal may not necessarily cause the underlying Direct3D 12 device to become removed.</span></span>

## <a name="debugging-directml-device-removal-and-other-errors"></a><span data-ttu-id="81e19-114">DirectML 裝置移除和其他錯誤的調試</span><span class="sxs-lookup"><span data-stu-id="81e19-114">Debugging DirectML device-removal, and other errors</span></span>

<span data-ttu-id="81e19-115">DirectML 錯誤的最常見原因是不正確 API 使用方式。</span><span class="sxs-lookup"><span data-stu-id="81e19-115">The most common cause of DirectML errors is invalid API usage.</span></span> <span data-ttu-id="81e19-116">不正確 API 使用方式可能會導致 **E_INVALIDARG** 的 HRESULT 錯誤碼，或可能導致裝置移除。</span><span class="sxs-lookup"><span data-stu-id="81e19-116">Invalid API usage might result in an **E_INVALIDARG** HRESULT error code, or it might result in device-removal.</span></span>

<span data-ttu-id="81e19-117">強烈建議您在開發期間啟用 [DirectML debug 層](dml-debug-layer.md) ，以便攔截和偵測這類錯誤。</span><span class="sxs-lookup"><span data-stu-id="81e19-117">We strongly recommend that you enable the [DirectML debug layer](dml-debug-layer.md) during your development, in order to catch and debug such errors.</span></span> <span data-ttu-id="81e19-118">DirectML debug 層會執行方法參數和 API 使用方式的廣泛驗證，而且會發出 debug 輸出訊息來協助您進行調試。</span><span class="sxs-lookup"><span data-stu-id="81e19-118">The DirectML debug layer performs extensive validation of method parameters and API usage, and it will emit debug output messages to help you debug.</span></span>

## <a name="see-also"></a><span data-ttu-id="81e19-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81e19-119">See also</span></span>

* [<span data-ttu-id="81e19-120">使用 DirectML debug layer</span><span class="sxs-lookup"><span data-stu-id="81e19-120">Using the DirectML debug layer</span></span>](dml-debug-layer.md)
