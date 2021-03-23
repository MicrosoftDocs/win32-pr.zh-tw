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
# <a name="handling-errors-and-device-removal-in-directml"></a>處理 DirectML 中的錯誤和裝置移除

## <a name="device-removal"></a>裝置-移除

如果發生無法復原的錯誤，DirectML 裝置可能會進入「裝置已移除」狀態。 導致裝置移除的無法復原錯誤包括不正確 API 使用方式 (針對未傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)) 、驅動程式錯誤、硬體錯誤或記憶體不足 (OOM) 條件的方法。

移除 DirectML 裝置時，裝置上的所有方法呼叫，以及該裝置所建立的每個物件都不會成為任何 ops。 如果是傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)的方法，則會傳回 [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/direct3ddxgi/dxgi-error) 錯誤碼。 您可以使用 [ **IDMLDevice：： GetDeviceRemovedReason** 方法](/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason)來檢查 DirectML 裝置是否已移除，並取得更詳細的錯誤碼。

除了釋出受影響的裝置及其所有子系，然後從頭重新建立 DirectML 裝置以外，您無法從裝置移除復原。

裝置移除基礎 Direct3D 12 裝置也會使 DirectML 裝置被移除。 不過，反向操作則不可行。 DirectML 裝置移除可能不一定會導致基礎 Direct3D 12 裝置被移除。

## <a name="debugging-directml-device-removal-and-other-errors"></a>DirectML 裝置移除和其他錯誤的調試

DirectML 錯誤的最常見原因是不正確 API 使用方式。 不正確 API 使用方式可能會導致 **E_INVALIDARG** 的 HRESULT 錯誤碼，或可能導致裝置移除。

強烈建議您在開發期間啟用 [DirectML debug 層](dml-debug-layer.md) ，以便攔截和偵測這類錯誤。 DirectML debug 層會執行方法參數和 API 使用方式的廣泛驗證，而且會發出 debug 輸出訊息來協助您進行調試。

## <a name="see-also"></a>另請參閱

* [使用 DirectML debug layer](dml-debug-layer.md)
