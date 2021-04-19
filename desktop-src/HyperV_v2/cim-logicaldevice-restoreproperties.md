---
description: 要求裝置從備份存放區重新建立其設定、設定及/或狀態資訊。
ms.assetid: 5a70f048-b335-4617-ae49-a99e728fa2e8
title: CIM_LogicalDevice 類別的 RestoreProperties 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.RestoreProperties
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c8298b4d88e3886c0f8d1321032f09379da7c9e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987765"
---
# <a name="restoreproperties-method-of-the-cim_logicaldevice-class"></a>CIM LogicalDevice 類別的 RestoreProperties 方法 \_

要求裝置從備份存放區重新建立其設定、設定及/或狀態資訊。 其目的是要透過 SaveProperties 方法) 在較早的時間來捕捉這項資訊 (，並使用它將裝置傳回到先前的「條件」。 並非所有裝置都支援此方法。 如果成功，方法應該會傳回0，如果要求不受支援則傳回1，如果發生任何其他錯誤，則傳回其他值。 在子類別中，可以使用方法上的 ValueMap 辨識符號來指定可能的傳回碼集。 您也可以在子類別中，以值陣列限定詞的形式指定可將 ValueMap 內容「轉譯」的字串。

## <a name="syntax"></a>語法


```mof
uint32 RestoreProperties();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

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

 

 




