---
description: 初始化選用元件管理員。
ms.assetid: 9a7ddca6-a6c8-4d96-81bb-66158b83ab68
title: OcInitialize 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcInitialize
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: aad102ac9881a801f693a429aab5dae07d09b5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999330"
---
# <a name="ocinitialize-function"></a>OcInitialize 函式

初始化選用元件管理員。

## <a name="syntax"></a>語法


```C++
PVOID OcInitialize(
  _In_  POCM_CLIENT_CALLBACKS Callbacks,
  _In_  LPCTSTR               MasterOcInfName,
  _In_  UINT                  Flags,
  _Out_ PBOOL                 ShowError,
  _In_  PVOID                 Log
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*回呼* \[在\]
</dt> <dd>

[**OCM \_ 用戶端 \_ 回呼**](ocm-client-callbacks.md)結構的指標，指定要讓 OC 管理員用來執行各種工作的回呼函數。

</dd> <dt>

*MasterOcInfName* \[在\]
</dt> <dd>

主要 OC .inf 檔案的路徑。

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

這個參數可以是下列一或多個值。

<dl> <dt>

<span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**OCINIT \_FORCENEWINF** (0x00000001) 
</dt> <dt>

<span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**OCINIT \_KILLSUBCOMPS** (0x00000002) 
</dt> <dt>

<span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**OCINIT \_RUNQUIET** (0x00000004) 
</dt> <dt>

<span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**OCINIT \_LANGUAGEAWARE** (0x00000008) 
</dt> </dl> </dd> <dt>

*ShowError* \[擴展\]
</dt> <dd>

如果函式失敗，這個參數會指出是否要顯示錯誤訊息。

</dd> <dt>

*記錄* \[ 檔在\]
</dt> <dd>

記錄的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

函數會傳回 OC 管理員內容值。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>OcManage.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**OCM \_ 用戶端 \_ 回呼**](ocm-client-callbacks.md)
</dt> <dt>

[**OcTerminate**](octerminate.md)
</dt> </dl>

 

 
