---
description: ActCtx 物件的 CreateObject 方法會在目前資訊清單的內容中建立物件。
ms.assetid: 531e6501-bb68-472b-b483-1f52815ba9d7
title: ActCtx. CreateObject 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.CreateObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2b4c4393d59ea5ab711dbf4bb1f4c88d906b6582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193289"
---
# <a name="actctxcreateobject-method"></a>ActCtx. CreateObject 方法

[**ActCtx**](microsoft-windows-actctx-object.md)物件的 **CreateObject** 方法會在目前資訊清單的內容中建立物件。

## <a name="syntax"></a>語法


```JScript
ActCtx.CreateObject(
  objectId
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*objectId* 
</dt> <dd>

字串，指定要建立之物件的類型。 例如，COM ProgID。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ IActCtx 定義為8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetObject 方法**](getobject.md)
</dt> </dl>

 

 




