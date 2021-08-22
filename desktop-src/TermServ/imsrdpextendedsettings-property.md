---
title: IMsRdpExtendedSettings 屬性屬性
description: 包含已命名的屬性。
ms.assetid: 3acaeff9-1617-46c3-80c3-b87496b83670
ms.tgt_platform: multiple
keywords:
- Property 屬性遠端桌面服務
- Property 屬性遠端桌面服務，IMsRdpExtendedSettings 介面
- IMsRdpExtendedSettings 介面遠端桌面服務，Property 屬性
topic_type:
- apiref
api_name:
- IMsRdpExtendedSettings.Property
- IMsRdpExtendedSettings.get_Property
- IMsRdpExtendedSettings.put_Property
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7deeb0e4d6d0f393bae09bacc9ff6709defe51bf6ca6128cbeb64e2f4f6e35cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138501"
---
# <a name="imsrdpextendedsettingsproperty-property"></a>IMsRdpExtendedSettings：:P roperty 屬性

包含已命名的屬性。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Property(
  [in]          BSTR    bstrPropertyName,
  [in]          VARIANT *pValue
);

HRESULT get_Property(
  [in]          BSTR    bstrPropertyName,
  [out, retval] VARIANT *pValue
);
```



## <a name="property-value"></a>屬性值

已命名的屬性值。

| 屬性名稱 | 資料類型 | Access | 可以在連接開始之後變更 | 描述 |
|----------|-----------|--------|-----------------------------------------|-------------|
| ConnectToChildSession | **VT \_ BOOL** | 讀取/寫入 | Yes | 將這個屬性設定為 **True** ，會導致用戶端控制項連接到本機電腦上的子會話，而不是遠端伺服器。 如果這個屬性設定為 **true**，您就無法連接到遠端伺服器，因為所有連接都會重新導向至 localhost。 如需子會話的詳細資訊，請參閱 [子會話](child-sessions.md)。 |
| DisableCredentialsDelegation | **VT \_ BOOL** | 讀取/寫入 | No | 若 **為 True**，則不會將認證傳送至遠端伺服器。 |
| EnableFrameBufferRedirection | **VT \_ BOOL** | 讀取/寫入 | No | 若 **為 True**，則會嘗試框架緩衝區重新導向。 若是回送連接 (相同電腦同時是用戶端和伺服器) 框架緩衝區重新導向，可讓框架緩衝區的記憶體在會話之間共用。 |
| EnableHardwareMode | **VT \_ BOOL**  | 僅限寫入 | No | 若 **為 True**，則會嘗試進行圖形解碼的硬體協助。 |
| IgnoreCursors | **VT \_ BOOL** | 僅限寫入 | No | 若 **為 True**，則會忽略遠端伺服器傳送的資料指標。 |
| ManualClipboardSyncEnabled | **VT \_ BOOL** | 讀取/寫入 | Yes | 將此屬性設定為 **True** 表示本機和遠端寫字板將不會自動保持同步。相反地，您必須使用 [**IMsRdpClipboard**](imsrdpclipboard.md) 介面，將剪貼簿格式從本機剪貼簿同步到遠端剪貼簿，並將遠端剪貼簿同步至本機剪貼簿。 |
| ZoomLevel | ***VT \_ UI4** | 讀取/寫入 | Yes | 使用 RDP ActiveX 控制項來實行縮放功能。 您可以從 RDP 的 **系統** 功能表使用 [縮放] 功能。 **ZoomLevel** 屬性在 RemoteApp 模式和全螢幕模式中沒有任何作用。 [**IMsRdpClientAdvancedSettings：： SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md) 和 **ZoomLevel** 彼此互斥。 |

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                                                                                                                                                                                                                           |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                                                                                                                                                                                                                                 |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                         |
| CLSID<br/>                    | CLSID \_ MsRdpClient7NotSafeForScripting 定義為54d38bf7-b1ef-4479-9674-1bd6ea465258<br/> CLSID \_ MsRdpClient8NotSafeForScripting 定義為 A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9NotSafeForScripting 定義為8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpExtendedSettings 定義為302D8188-0052-4807-806A-362B628F9AC5<br/>                                                                                                                                                                                                                      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpExtendedSettings**](imsrdpextendedsettings.md)
</dt> </dl>

 

 





