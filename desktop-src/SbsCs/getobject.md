---
description: GetObject 方法會取得現有 ActCtx 物件的實例。
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
ms.openlocfilehash: 11b71d8d40d947472612c91f70e9956aa7798806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690159"
---
# <a name="actctxgetobject-method"></a>ActCtx 的 GetObject 方法

**GetObject** 方法會取得現有 [**ActCtx**](microsoft-windows-actctx-object.md)物件的實例。

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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ IActCtx 定義為8FA7728F-B69B-4EE5-99F2-E2AA021BEF28<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CreateObject 方法**](createobject.md)
</dt> </dl>

 

 




