---
description: 密碼編譯服務提供者 (CSP) 用來驗證 DLL 的簽章。
ms.assetid: 477a6c9f-05ac-485a-8b27-5605fc11c1d6
title: 'CRYPT_VERIFY_IMAGE 函式指標 (Cspdk) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_VERIFY_IMAGE
- CRYPT_VERIFY_IMAGE_A
- CRYPT_VERIFY_IMAGE_W
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: b33e6e627c87840e4adb7615f7e3ca5932a7402a3b3ae7110be51c0847a5f67f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006676"
---
# <a name="crypt_verify_image-function-pointer"></a>CRYPT \_ 驗證 \_ 影像函式指標

[*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 使用 **FuncVerifyImage** 回呼函式來驗證 DLL 的簽章。

CSP 進行函式呼叫的所有輔助 Dll 都必須以相同的方式進行簽署， (以及與主要 CSP DLL) 的金鑰相同。 若要確保這個簽章，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式，以動態方式載入輔助 dll。 但是在載入 DLL 之前，必須先驗證 DLL 的簽章。 CSP 會藉由呼叫 **FuncVerifyImage** 函式來執行這項驗證，如下列範例所示。

## <a name="syntax"></a>語法


```C++
typedef BOOL ( WINAPI *CRYPT_VERIFY_IMAGE)(
  _In_       LPCTSTR lpszImage,
  _In_ const BYTE    *pbSigData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpszImage* \[在\]
</dt> <dd>

以 null 終止之字串的位址，其中包含要驗證簽章之 DLL 的路徑和檔案名。

</dd> <dt>

*pbSigData* \[在\]
</dt> <dd>

包含簽章之緩衝區的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回 **TRUE** ，否則會傳回 **FALSE** 。

## <a name="examples"></a>範例

下列範例示範如何使用 **FuncVerifyImage** 回呼函式，在 CSP 載入 DLL 之前先驗證其簽章。


```C++
BOOL (FARPROC *ProvVerifyImage)(LPCSTR lpszImage, BYTE *pSigData);


//  "ProvVerifyImage" has been set to "pVTable->FuncVerifyImage"
//  within the CPAcquireContext function.

//  bSignature is a previously assigned BYTE array that contains the
//  signature that is stored in the C:\Winnt40\System32\signature.sig
//  file. During development, this file is created with the 
//  Sign.exe tool.
...


//  Verify the signature in the
//  C:\Winnt40\System32\Signature.dll file.
if(RCRYPT_FAILED(ProvVerifyImage
    ("c:\\winnt40\\system32\\signature.dll",
        bSignature)) {
    SetLastError(NTE_BAD_SIGNATURE);
    return CRYPT_FAILED;
}

//  Load the DLL with the LoadLibrary function, then acquire pointers 
//  to the functions with the GetProcAddress function.
//...
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Cspdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CPAcquireCoNtext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**VTableProvStruc**](vtableprovstruc.md)
</dt> </dl>

 

 
