---
description: 此函式會捕獲離線登錄庫的版本。
ms.assetid: 625f088a-db5e-47ea-aa48-39b1c70cf15b
title: 'ORGetVersion 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetVersion
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: d909013d88c9a3abbe91f152e1333fb5faf35852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978719"
---
# <a name="orgetversion-function"></a>ORGetVersion 函式

此函式會捕獲離線登錄庫的版本。

## <a name="syntax"></a>語法


```C++
VOID ORGetVersion(
  _Out_ PDWORD pdwMajorVersion,
  _Out_ PDWORD pdwMinorVersion
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdwMajorVersion* \[擴展\]
</dt> <dd>

變數的指標，用來接收離線登錄庫的主要版本。 針對程式庫的初始版本，值為1。

</dd> <dt>

*pdwMinorVersion* \[擴展\]
</dt> <dd>

變數的指標，用來接收離線登錄庫的次要版本。 若為程式庫的初始版本，此值為0。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|---------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Offline Registry library 1.0 版或更新版本<br/>                      |
| 標頭<br/>          | <dl> <dt>Offreg。h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



 

 




