---
description: 資訊清單屬性是用來設定或取得主動啟用內容。
ms.assetid: 5ad16c7b-3d66-4083-bc0f-f8294757764f
title: ActCtx 資訊清單屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.Manifest
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2ebc671bbfcdfc951343e7f92cc0385ace43997e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943345"
---
# <a name="actctxmanifest-property"></a>ActCtx 資訊清單屬性

**資訊清單** 屬性是用來設定或取得主動啟用內容。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = ActCtx.Manifest
```



## <a name="property-value"></a>屬性值

## <a name="remarks"></a>備註

如果可以使用提供的資訊清單檔來建立啟用內容，下列腳本會設定資訊清單屬性，並啟動資訊清單所指定的啟用常數。 如果無法從資訊清單建立啟用內容，啟用內容仍會設定為目前作用中的啟用內容。

ActCtxObj。資訊清單 = "<*資訊清單檔案名*>";

如果先前已建立或啟用啟用內容，下列腳本會將 **資訊清單** 屬性設定為目前的啟用內容。 如果先前未建立或啟用啟用內容，這會將 **資訊清單** 屬性設定為空字串。

"BSTR bstrManifest = ActCtxObj"

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ IActCtx 定義為8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



 

 




