---
description: 搭配 Rundll32.exe 使用時，會啟動 Passport Wizard。
title: PassportWizardRunDll 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PassportWizardRunDll
api_type:
- DllExport
api_location:
- Netplwiz.dll
ms.assetid: 015c3875-698e-4d80-bbfc-4fc8a71197b7
ms.openlocfilehash: 7b75f4f3371814d00cf5b58dc12854763318c7ee424f35c7a7e6dad9f7734058
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820618"
---
# <a name="passportwizardrundll-function"></a>PassportWizardRunDll 函式

\[您可以透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 來取得此函式。 它可能會在 Windows 的後續版本中變更或無法使用。\]

搭配 Rundll32.exe 使用時，會啟動 Passport Wizard。

## <a name="syntax"></a>語法


```C++
void PassportWizardRunDll(
  _In_ HWND      hwndStub,
  _In_ HINSTANCE hAppInstance,
  _In_ LPTSTR    lpszCmdLine,
  _In_ int       nCmdShow
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwndStub* \[在\]
</dt> <dd>

類型： **HWND**

主控視窗的控制碼。 此參數通常會設定為 **Null**。

</dd> <dt>

*hAppInstance* \[在\]
</dt> <dd>

類型： **HINSTANCE**

程式庫檔案的控制碼，以 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ( "netplwiz" ) 的傳回值形式取得。

</dd> <dt>

*lpszCmdLine* \[在\]
</dt> <dd>

類型： **LPTSTR**

引數資料。 這個值一律是空的。

</dd> <dt>

*nCmdShow* \[在\]
</dt> <dd>

類型： **int**

設定視窗的顯示模式。

</dd> </dl>

## <a name="return-value"></a>傳回值

無。

## <a name="remarks"></a>備註

Passport Wizard 可用來取得 Windows 的預設 Passport。 Passport 可讓使用者使用使用者的電子郵件地址，個人化存取所有的 MSN 網站和其他具備 Passport 功能的網站。 透過 Rundll32.exe 命令使用 **PassportWizardRunDll** 做為 Netplwiz.dll 檔案的進入點，可讓您從命令列啟動 Passport Wizard，就好像它是可執行檔一樣。

**PassportWizardRunDll** 只會在 Rundll32.exe 命令的內容中使用，如下所示：

**rundll32.exe netplwiz.dll、PassportWizardRunDll**

使用進入點函式搭配 Rundll32.exe 不像一般函式呼叫。 函式名稱和儲存的 .dll 檔案名，只會用來做為命令列參數。 在 [語法] 下顯示的函式定義，只是您可以使用 Rundll32.exe 呼叫的所有函式的標準原型。 *HwndStub*、 *hAppInstance* 和 *nCmdShow* 的特定值不是由使用者提供，而是由 rundll32.exe 在幕後處理。 **PassportWizardRunDll** 不會使用 *lpszCmdLine* 值，因此不需要額外的資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                            |
| 標頭<br/>                   | <dl> <dt>None</dt> </dl>                                 |
| DLL<br/>                      | <dl> <dt>Netplwiz.dll (5.60 版或更新版本) </dt> </dl> |



 

 
