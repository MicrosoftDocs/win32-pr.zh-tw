---
title: IMsRdpDriveCollection DriveCount 屬性
description: 抓取集合中的物件計數。 |IMsRdpDriveCollection DriveCount 屬性
ms.assetid: 33b39657-2cc1-4f1e-b23a-809a9737ed8d
ms.tgt_platform: multiple
keywords:
- DriveCount 屬性遠端桌面服務
- DriveCount 屬性遠端桌面服務，IMsRdpDriveCollection 介面
- IMsRdpDriveCollection 介面遠端桌面服務，DriveCount 屬性
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveCount
- IMsRdpDriveCollection.get_DriveCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af724344cd7d88676483c13d1a6a8cfeb8548294
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106991433"
---
# <a name="imsrdpdrivecollectiondrivecount-property"></a>IMsRdpDriveCollection：:D riveCount 屬性

抓取集合中的物件計數。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_DriveCount(
  [out] ULONG *pDriveCount
);
```



## <a name="property-value"></a>屬性值

物件計數。

## <a name="error-codes"></a>錯誤碼

如果方法成功，則會傳回 **S \_ OK** 。 任何其他 **HRESULT** 值都表示呼叫失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpDriveCollection 定義為 7ff17599-da2c-4677-ad35-f60c04fe1585<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

 





