---
description: 取得符合所指定雜湊的雜湊識別規則層級。
ms.assetid: 1592c8da-31c0-45fb-b832-d439dd53c277
title: SaferiSearchMatchingHashRules 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SaferiSearchMatchingHashRules
api_type:
- DllExport
api_location:
- Advapi32.dll
- Ext-MS-Win-AdvAPI32-safer-l1-1-0.dll
ms.openlocfilehash: 2d1b7a2b2ce3f0f0e45d87a46219f3ee4d999bc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468409"
---
# <a name="saferisearchmatchinghashrules-function"></a>SaferiSearchMatchingHashRules 函式

取得符合所指定雜湊的雜湊識別規則層級。

此函數沒有相關聯的匯入程式庫，而且未在公用標頭中宣告。 您必須使用這個函式的簽章來定義函式指標，而且您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函式，以動態方式連結至 Advapi32.dll。

我們建議使用 [**SaferIdentifyLevel**](/windows/win32/api/winsafer/nf-winsafer-saferidentifylevel) 函式來評估軟體限制原則。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI SaferiSearchMatchingHashRules(
  _In_opt_ ALG_ID HashAlgorithm,
  _In_     PBYTE  pHashBytes,
  _In_     DWORD  dwHashSize,
  _In_opt_ DWORD  dwOriginalImageSize,
  _Out_    PDWORD pdwFoundLevel,
           PDWORD pdwSaferFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*HashAlgorithm* \[在中，選擇性\]
</dt> <dd>

用來建立雜湊之演算法的識別碼。

</dd> <dt>

*pHashBytes* \[在\]
</dt> <dd>

包含雜湊的位元組陣列指標。

</dd> <dt>

*dwHashSize* \[在\]
</dt> <dd>

*PHashBytes* 陣列的大小（以位元組為單位）。

</dd> <dt>

*dwOriginalImageSize* \[在中，選擇性\]
</dt> <dd>

計算雜湊之原始影像的大小（以位元組為單位）。

</dd> <dt>

*pdwFoundLevel* \[擴展\]
</dt> <dd>

符合雜湊識別碼規則之層級識別碼的指標。

</dd> <dt>

*pdwSaferFlags* 
</dt> <dd>

保留的。 將此值設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則 **為 TRUE** ;否則 **為 FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Advapi32.dll</dt> </dl> |



 

 
