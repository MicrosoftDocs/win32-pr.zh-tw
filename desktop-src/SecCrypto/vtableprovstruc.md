---
description: 包含回呼函式的指標，這些函式可供密碼編譯服務提供者 (CSP) 函式使用。
ms.assetid: 84a379e9-c6b9-4c1d-bbbb-9bed4a045d90
title: 'VTableProvStruc 結構 (Cspdk .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VTableProvStruc
- VTableProvStrucW
api_type:
- HeaderDef
api_location:
- Cspdk.h
ms.openlocfilehash: 2815d12735023cd0f7ac60fc2ed9f60fc56e32d0f54610f295a2e6b0544e589c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117970864"
---
# <a name="vtableprovstruc-structure"></a>VTableProvStruc 結構

**VTableProvStruc** 結構包含回呼函式的指標，可供 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 函式使用。

## <a name="syntax"></a>語法


```C++
typedef struct VTableProvStruc {
  DWORD   Version;
  FARPROC FuncVerifyImage;
  FARPROC FuncReturnhWnd;
  DWORD   dwProvType;
  BYTE    *pbContextInfo;
  DWORD   cbContextInfo;
  LPSTR   pszProvName;
} VTableProvStruc, *PVTableProvStruc;
```



## <a name="members"></a>成員

<dl> <dt>

**版本**
</dt> <dd>

表示結構版本的 **DWORD** 值。 使用這個結構的三個版本。 版本為數字1、2和3，並決定結構的哪些成員有效。 第1版的成員在所有支援此結構的系統上都有效。

這是第1版的成員。

</dd> <dt>

**FuncVerifyImage**
</dt> <dd>

[**FuncVerifyImage**](funcverifyimage.md)回呼函式的位址，csp 會使用此函式來驗證 csp 將載入之任何 dll 的簽章。 CSP 進行函式呼叫的所有輔助 Dll 都必須以相同的方式進行簽署， (以及與主要 CSP DLL) 的金鑰相同。 若要確保這個簽章，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式，以動態方式載入輔助 dll。 但是在載入 DLL 之前，必須先驗證 DLL 的簽章。 CSP 會藉由呼叫 **FuncVerifyImage** 函式來執行這項驗證，如下列範例所示。

您可以儲存並使用這個函式指標，直到發行 CSP 內容為止。

這是第1版的成員。

</dd> <dt>

**FuncReturnhWnd**
</dt> <dd>

[**FuncReturnhWnd**](funcreturnhwnd.md)回呼函式的位址，這個函式會傳回 CSP 應使用的視窗控制碼做為顯示之任何使用者介面的父系或擁有者。 未直接與使用專用硬體的使用者和 Csp 通訊的 Csp 可以忽略此專案。 此視窗控制碼預設為零，但應用程式可以使用 [**CryptSetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam) 函式設定 **PP \_ 用戶端 \_ HWND** 屬性，將此值設定為不同的值。

您可以儲存並使用這個函式指標，直到發行 CSP 內容為止。

這是第1版的成員。

</dd> <dt>

**dwProvType**
</dt> <dd>

**DWORD** 值，指定要取得的提供者類型。 下列 [*提供者類型*](../secgloss/p-gly.md) 已預先定義，並會在 [CSP 互通性](https://www.bing.com/search?q=CSP+Interoperability)中詳細討論：

-   >PROV \_ RSA \_ FULL
-   >PROV \_ RSA \_ SIG
-   >PROV \_ DSS
-   >PROV \_ FORTEZZA
-   >PROV \_ MS \_ EXCHANGE

這是第2版的成員。

</dd> <dt>

**pbCoNtextInfo**
</dt> <dd>

內容資訊陣列的指標。 **PbCoNtextInfo** 和 **cbCoNtextInfo** 成員一起決定使用 PP 內容資訊集呼叫 [**CPSetProvParam**](https://www.bing.com/search?q=**CPSetProvParam**)函式時所使用的資訊集 \_ \_ 。

這是第2版的成員。

</dd> <dt>

**cbCoNtextInfo**
</dt> <dd>

**DWORD** 值，指出 **pbCoNtextInfo** 陣列中的元素數目。

這是第2版的成員。

</dd> <dt>

**pszProvName**
</dt> <dd>

字串，其中包含提供者的名稱。

這是第3版的成員。

</dd> </dl>

## <a name="remarks"></a>備註

**VTableProvStruc** 結構中的指標只能在 [**CPAcquireCoNtext**](https://www.bing.com/search?q=**CPAcquireContext**)函數中使用。 如果在呼叫 **CPAcquireCoNtext** 完成後需要結構的成員，則 CSP 必須建立所需結構元素的複本。 您可以儲存和使用此結構中的函式指標，直到發行 CSP 內容為止。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Cspdk。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **VTableProvStrucW** (Unicode) <br/>                                          |



 

 
