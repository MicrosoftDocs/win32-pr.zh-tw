---
description: 要求裝置在備份存放區中捕獲其目前的設定、設定及/或狀態資訊。
ms.assetid: e47aea90-06f9-441c-bb30-aa742b49ce72
title: CIM_LogicalDevice 類別的 SaveProperties 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SaveProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e5910ea87a6321872b009003bf18d26910b53627dba6c51647f2896dde2e686
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648160"
---
# <a name="saveproperties-method-of-the-cim_logicaldevice-class"></a>CIM LogicalDevice 類別的 SaveProperties 方法 \_

要求裝置在備份存放區中捕獲其目前的設定、設定及/或狀態資訊。 目標是在稍後透過 RestoreProperties 方法) 來使用這項資訊 (，以將裝置傳回到其目前的「條件」。 並非所有裝置都支援此方法。 如果成功，方法應該會傳回0，如果要求不受支援則傳回1，如果發生任何其他錯誤，則傳回其他值。 在子類別中，可以使用方法上的 ValueMap 辨識符號來指定可能的傳回碼集。 您也可以在子類別中，以值陣列限定詞的形式指定可將 ValueMap 內容「轉譯」的字串。

## <a name="syntax"></a>語法


```mof
uint32 SaveProperties();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

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

 

 




