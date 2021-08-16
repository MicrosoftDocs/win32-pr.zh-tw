---
description: 釋放在流覽 applet 時可能耗用的 JAVA 類別載入器。
ms.assetid: f6d5e8b9-4c0b-4533-8bf7-070b8c2e6681
title: NotifyBrowserShutdown 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NotifyBrowserShutdown
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 60f361d8f9963081c4af2a840a01eb29f9946eb064cad2335f95b3622932add1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826814"
---
# <a name="notifybrowsershutdown-function"></a>NotifyBrowserShutdown 函式

釋放在流覽 applet 時可能耗用的 JAVA 類別載入器。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI NotifyBrowserShutdown(
   LPVOID lpvReserved
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpvReserved* 
</dt> <dd>

不使用這個參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 **S \_ OK**。 否則，傳回值會是錯誤碼。

## <a name="remarks"></a>備註

當瀏覽器視窗的計數在整合式 Web 模式下達到零時，此函式會釋出 JAVA 類別載入器。 當使用者再次開始流覽 applet 時，JAVA VM 將會下載最新的類別檔案。

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjava.dll</dt> </dl> |



 

 
