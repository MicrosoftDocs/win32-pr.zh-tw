---
title: IMsRdpDrive Name 屬性
description: 抓取磁片磁碟機的名稱。
ms.assetid: 5aabb7df-fd46-48aa-ad1d-51da45495782
ms.tgt_platform: multiple
keywords:
- Name 屬性遠端桌面服務
- Name 屬性遠端桌面服務，IMsRdpDrive 介面
- IMsRdpDrive 介面遠端桌面服務，Name 屬性
topic_type:
- apiref
api_name:
- IMsRdpDrive.Name
- IMsRdpDrive.get_Name
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bde69814f38c39315a02a76bd52b8c3c38baffc2c0a92601ef383cb60b0bc492
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125638"
---
# <a name="imsrdpdrivename-property"></a>IMsRdpDrive：： Name 屬性

抓取磁片磁碟機的名稱。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Name(
  [out] BSTR *pName
);
```



## <a name="property-value"></a>屬性值

磁片磁碟機名稱。

## <a name="error-codes"></a>錯誤碼

如果方法成功，則會傳回 **S \_ OK** 。 任何其他 **HRESULT** 值都表示呼叫失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDrive 定義為 d28b5458-f694-47a8-8e61-40356a767e46<br/>         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpDrive**](imsrdpdrive.md)
</dt> </dl>

 

 





