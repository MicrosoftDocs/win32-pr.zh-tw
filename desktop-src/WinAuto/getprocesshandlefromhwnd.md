---
title: GetProcessHandleFromHwnd 函式
description: 從視窗控制碼抓取進程控制碼。
ms.assetid: 173579d2-c930-402c-81c7-761b063b5b51
keywords:
- GetProcessHandleFromHwnd 函式 Windows 的協助工具
topic_type:
- apiref
api_name:
- GetProcessHandleFromHwnd
api_location:
- Oleacc.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4096f77b4295e9567f17f747a5aee1edae1b592cb49c89547102cb6d017b7814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860348"
---
# <a name="getprocesshandlefromhwnd-function"></a>GetProcessHandleFromHwnd 函式

從視窗控制碼抓取進程控制碼。

## <a name="syntax"></a>語法


```C++
HANDLE WINAPI GetProcessHandleFromHwnd(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwnd* \[在\]
</dt> <dd>

類型： **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**

視窗控制代碼 (Window Handle)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[**控制碼**](/windows/desktop/WinProg/windows-data-types)**

如果成功，會傳回擁有視窗之進程的控制碼。

如果不成功，則傳回 **Null**。

## <a name="remarks"></a>備註

在舊版作業系統中，進程可以開啟另一個進程 (存取其記憶體，例如) 使用 [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess)。 如果呼叫端具有適當的許可權，則此函式會成功;呼叫端和目標進程通常必須是相同的使用者。

不過，在 Windows Vista 中， [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess)會在呼叫端具有 UIAccess 的情況下失敗，並提高目標進程的許可權。 在此情況下，目標進程的擁有者是在 Administrators 群組中，但呼叫進程正在以受限制的權杖執行，因此沒有此群組的成員資格，而且會被拒絕存取提升的進程。 但是，如果呼叫端具有 UIAccess，則可以使用 windows 攔截將程式碼插入目標進程，然後從目標進程內，將控制碼傳回給呼叫端。

**GetProcessHandleFromHwnd** 是一個便利的函式，它會使用這項技術來取得擁有指定 HWND 之進程的控制碼。 請注意，只有在呼叫端和目標進程以相同使用者的形式執行時，才會成功。 傳回的控制碼具有下列許可權：進程 \_ 重複 \_ 處理 \| 進程 \_ vm \_ 作業 \| 進程 vm \_ 讀取程式 \_ \| \_ vm \_ 寫入 \| 同步處理。 如果需要其他許可權，則可能需要明確地執行攔截技術，而不是使用此函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Oleacc.dll</dt> </dl> |



 

