---
description: 停用功能。
ms.assetid: 2ea2dcfb-84e6-4f83-9afd-c3050b53f37c
title: pSetupSetGlobalFlags 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupSetGlobalFlags
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 6fcb56f26d5aea233156e0fe3dfab13099d29df7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991201"
---
# <a name="psetupsetglobalflags-function"></a>pSetupSetGlobalFlags 函式

\[在 Windows Vista 或 Windows Server 2008 中無法使用此功能。\]

停用功能。

## <a name="syntax"></a>語法


```C++
VOID pSetupSetGlobalFlags(
  _In_ DWORD Value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*值* \[在\]
</dt> <dd>

用來停用使用者介面或自動備份的旗標。



| 值                                                                                                                                                                                                                                         | 意義                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PSPGF_NONINTERACTIVE"></span><span id="pspgf_noninteractive"></span><dl> <dt>**PSPGF \_非互動式**</dt> <dt>0x004</dt> </dl> | 設定為 [停用使用者介面]。<br/>   |
| <span id="PSPGF_NO_BACKUP"></span><span id="pspgf_no_backup"></span><dl> <dt>**PSPGF \_沒有 \_ 備份**</dt> <dt>0x002</dt> </dl>               | 設定為 [停用自動備份]。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Setupapi.dll</dt> </dl> |



 

 
