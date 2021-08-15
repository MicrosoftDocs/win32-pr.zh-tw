---
description: DeleteExtractedFiles 函式會刪除解壓縮函數所解壓縮的檔案。
ms.assetid: 253e6267-d4be-46d6-bad2-2eb20bbc7e33
title: DeleteExtractedFiles 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeleteExtractedFiles
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: 500de4df41c82f1956f50abcc25dc84f11484b693dc8d1a5f8bc53ab556ade0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162089"
---
# <a name="deleteextractedfiles-function"></a>DeleteExtractedFiles 函式

\[不再支援此函式，因此無法保證其行為。\]

**DeleteExtractedFiles** 函式會刪除 [**解壓縮**](extract.md)函數所解壓縮的檔案。

## <a name="syntax"></a>語法


```C++
VOID WINAPI DeleteExtractedFiles(
   PSESSION ps
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*Ps* 
</dt> <dd>

[**會話**](session.md)結構的指標，其中包含目前會話的相關資訊。

此函式會釋出此結構之 **pFileList** 成員中的記憶體，並將 **PFileList** 設定為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**擷取**](extract.md)
</dt> <dt>

[**會話**](session.md)
</dt> </dl>

 

 
