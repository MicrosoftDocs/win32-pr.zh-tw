---
title: DXCoreNotificationType
description: 定義常數，指定 [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) 或 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) 物件所引發的通知類型。
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3eacd77d2cf15c78a0dc959285874de943fd9130
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092817"
---
# <a name="dxcorenotificationtype-enum"></a>DXCoreNotificationType 列舉

定義常數，指定 [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) 或 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) 物件所引發的通知類型。

您可以分別呼叫 [IDXCoreAdapterFactory：： RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) 和 [IDXCoreAdapterFactory：： UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)，來註冊及取消註冊這些通知。

## <a name="syntax"></a>Syntax

```cpp
enum class DXCoreNotificationType : uint32_t
{
  AdapterListStale = 0,
  AdapterNoLongerValid = 1,
  AdapterBudgetChange = 2,
  AdapterHardwareContentProtectionTeardown = 3
};
```

## <a name="constants"></a>常數

### <a name="adapterliststale"></a>AdapterListStale

當介面卡清單變得過時時， <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist">IDXCoreAdapterList</a> 物件會引發這項通知。 最新到過時的轉換是單向的，一次，因此最多隻會引發一次這項通知。

### <a name="adapternolongervalid"></a>AdapterNoLongerValid

當介面卡不再有效時， <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> 物件就會引發此通知。 有效轉換不正確轉換是單向的，而這項通知最多隻會引發一次。

### <a name="adapterbudgetchange"></a>AdapterBudgetChange

此通知是在介面卡預算變更發生時由 <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> 物件引發。 此通知可能會發生多次。 使用此通知的功能與 <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent">IDXGIAdapter3：： RegisterVideoMemoryBudgetChangeNotificationEvent</a>類似。 若要回應此事件，您應該呼叫 [IDXCoreAdapter：： QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) (搭配 [DXCoreAdapterState：： AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md)) 來評估目前的記憶體預算狀態。

### <a name="adapterhardwarecontentprotectionteardown"></a>AdapterHardwareContentProtectionTeardown

<a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a>物件會引發此通知，以通知介面卡的硬體內容保護卸載。 此通知可能會發生多次。 其功能類似于 <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registerhardwarecontentprotectionteardownstatusevent">IDXGIAdapter3：： RegisterHardwareContentProtectionTeardownStatusEvent</a>。 為了回應此事件，您應該重新評估目前的加密會話狀態;例如，藉由呼叫 [ID3D11VideoCoNtext1：： CheckCryptoSessionStatus](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) 來判斷特定 [ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) 介面之硬體清除的影響。

## <a name="see-also"></a>另請參閱

[IDXCoreAdapterFactory：： RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)、 [IDXCoreAdapterFactory：： UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)、 [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md)、 [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md)、 [DXCore 參考](../dxcore-reference.md)、 [使用 DXCore 來列舉介面卡](../dxcore-enum-adapters.md)