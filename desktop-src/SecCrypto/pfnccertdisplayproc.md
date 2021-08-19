---
description: 使用者定義的回呼函式，可讓 CryptUIDlgSelectCertificate 函式的呼叫者處理使用者選取要查看的憑證顯示。
ms.assetid: fdb9e9e0-02f1-42e0-9a11-204d916a1a88
title: PFNCCERTDISPLAYPROC 回呼函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PFNCCERTDISPLAYPROC
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: a0d78569990874c87082d57045cf8075043c6edccc96b507d2d8dc72a58fb379
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978974"
---
# <a name="pfnccertdisplayproc-callback-function"></a>PFNCCERTDISPLAYPROC 回呼函式

**PFNCCERTDISPLAYPROC** 函式是使用者定義的回呼函式，可讓 [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md)函式的呼叫者處理使用者選取要查看的憑證顯示。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI * PFNCCERTDISPLAYPROC(
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ HWND           hWndSelCertDlg,
  _In_ void           *pvCallbackData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCertCoNtext* \[在\]
</dt> <dd>

憑證 [**\_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) 結構的指標，表示要顯示的憑證。

</dd> <dt>

*hWndSelCertDlg* \[在\]
</dt> <dd>

對話方塊的控制碼，此對話方塊會選取憑證來進行查看。

</dd> <dt>

*pvCallbackData* \[在\]
</dt> <dd>

回呼函數所使用的其他資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式會傳回 **TRUE** ，表示它會處理憑證的顯示，而且對話方塊不應顯示憑證。 如果此函數傳回 **FALSE**，則對話方塊會顯示憑證。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |



 

 




