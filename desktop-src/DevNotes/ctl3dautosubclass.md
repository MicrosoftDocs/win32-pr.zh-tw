---
description: 自動子類別，並將3D 效果加入至應用程式中的所有對話方塊。
ms.assetid: 96555052-c564-4cc7-9b24-e527f8e2f879
title: Ctl3dAutoSubclass 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 85f4c85d1d608ff97147a935806b090162f5a78a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979465"
---
# <a name="ctl3dautosubclass-function"></a>Ctl3dAutoSubclass 函式

自動子類別，並將3D 效果加入至應用程式中的所有對話方塊。

## <a name="syntax"></a>語法


```C++
PUBLIC BOOL FAR PASCAL Ctl3dAutoSubclass(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hinstApp* 
</dt> <dd>

要註冊為用戶端之應用程式的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

除非下列其中一個條件存在，否則會傳回 **TRUE** ，在此情況下，它會傳回 **FALSE**：

-   CTL3D 正在 Windows 3.0 版或更早版本下執行。
-   CTL3D 目前的應用程式在其資料表中沒有可用的空間。 CTL3D 可同時服務多達32的應用程式。
-   CTL3D 無法安裝其 CBT 勾點。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
