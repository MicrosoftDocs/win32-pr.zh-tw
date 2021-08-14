---
description: EnableDevice 方法已被取代，而不是與這個方法所提供的功能直接重迭的一般 RequestStateChange 方法。
ms.assetid: 1d481417-b640-437d-82ed-d45a9e420d3b
title: CIM_LogicalDevice 類別的 EnableDevice 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.EnableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a01d1b206d0d38f74c5701c8c088506792cb6ca6f997b9e0280adcc61e5a8633
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648523"
---
# <a name="enabledevice-method-of-the-cim_logicaldevice-class"></a>CIM LogicalDevice 類別的 EnableDevice 方法 \_

EnableDevice 方法已被取代，而不是與這個方法所提供的功能直接重迭的一般 RequestStateChange 方法。

要求啟用 LogicalDevice ( "Enabled" 輸入參數 = TRUE) 或停用 (= FALSE) 。 如果成功，裝置的 StatusInfo/EnabledState 屬性應該會反映預期狀態 (啟用/停用) 。 請注意，這個方法的函式與 RequestedState 屬性重迭。 在模型中加入了 RequestedState 來維護記錄， (也就是最後一個狀態要求的保存值) 。 叫用 EnableDevice 方法應該適當地設定 RequestedState 屬性。

如果要求成功執行，傳回碼應為0，如果不支援要求則為1，如果發生錯誤，則為其他值。 在子類別中，可以使用方法上的 ValueMap 辨識符號來指定可能的傳回碼集。 您也可以在子類別中，以值陣列限定詞的形式指定可將 ValueMap 內容「轉譯」的字串。

## <a name="syntax"></a>語法


```mof
uint32 EnableDevice(
  [in] boolean Enabled
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*已啟用* \[在\]
</dt> <dd>

若為 TRUE，則啟用裝置，如果為 FALSE，則停用裝置。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回 0;否則，會傳回錯誤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

 




