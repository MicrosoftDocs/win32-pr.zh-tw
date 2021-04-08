---
UID: ''
title: UnicodeToBytes 函式
description: 將 Unicode 字元轉換成 GB18030 位元組。
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: WideCharToMultiByte, MultiByteToWideChar
ms.topic: reference
req.header: Gb18030.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: c_g18030.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- c_g18030.dll
api_name:
- UnicodeToBytes
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 66ed21768c3acef7f2aa2128df057da8552b2ad2
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2020
ms.locfileid: "103679503"
---
# <a name="unicodetobytes-function"></a>UnicodeToBytes 函式

## <a name="description"></a>Description

已取代。 將 Unicode 字元轉換成 GB18030 位元組。

**注意**  將 Unicode 字元轉換成 GB18030 位元組時，要在 Windows Vista 和更新版本上執行的應用程式應該使用 [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) 函式。

```cpp
DWORD UnicodeToBytes(
  _In_ LPWSTR lpWideCharStr,
  _In_ UINT   cchWideChar,
  _In_ LPSTR  lpMultiByteStr,
  _In_ UINT   cchMultiByte
);
```

## <a name="parameters"></a>參數

### <a name="lpwidecharstr-in"></a>lpWideCharStr [in]

要轉換的 Unicode 字串指標。

### <a name="cchwidechar-in"></a>cchWideChar [in]

要轉換的 Unicode 字串的字元計數。

### <a name="lpmultibytestr-in"></a>lpMultiByteStr [in]

目標多位元組緩衝區的指標。
如果 *lpMultiByteStr* 為0，則會傳回 GB18030 結果的位元組計數，且不會進行任何轉換。

### <a name="cchmultibyte-in"></a>cchMultiByte [in]

目標多位元組緩衝區的位元組計數。
如果 *cchMultiByte* 為0，則會傳回 GB18030 結果的位元組計數，且不會進行任何轉換。

## <a name="returns"></a>傳回

如果成功，則傳回所產生之多位元組字元的位元組計數。

## <a name="remarks"></a>備註

## <a name="see-also"></a>另請參閱

[WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)

[MultiByteToWideChar](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
