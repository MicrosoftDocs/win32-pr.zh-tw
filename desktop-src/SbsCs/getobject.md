---
description: GetObject 方法會取得現有 Microsoft 的實例。Windows。ActCtx 物件。
ms.assetid: 547525f3-afef-463b-823a-df8ccd954f36
title: ActCtx 的 GetObject 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.GetObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: a102fdae74232fa9a67c4b9455050bcdba32a219d8a66180ae8bc6ce6cb96c8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885278"
---
# <a name="actctxgetobject-method"></a>ActCtx 的 GetObject 方法

**GetObject** 方法會取得現有 Microsoft Windows 的實例 [**。ActCtx**](microsoft-windows-actctx-object.md)物件。

## <a name="syntax"></a>語法


```JScript
ActCtx.GetObject(
  bstrName
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrName* 
</dt> <dd>

表示物件的必要字串。 此名稱必須位於 **HKEY \_ LOCAL \_ MACHINE** \\ **Microsoft** \\ **Visual Studio** \\ **6.0** \\ **<package>** \\ **Automation** 下的登錄中。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ IActCtx 定義為8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CreateObject 方法**](createobject.md)
</dt> </dl>

 

 




