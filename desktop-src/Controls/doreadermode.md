---
title: DoReaderMode 函式
description: 在視窗中啟用讀取器模式。
ms.assetid: 8f898cdd-c907-430a-8287-15d88390c756
keywords:
- DoReaderMode 函式 Windows 控制項
topic_type:
- apiref
api_name:
- DoReaderMode
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5f5c5863e804cd4bbaab651447e4c6f22dc24a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467128"
---
# <a name="doreadermode-function"></a>DoReaderMode 函式

\[**DoReaderMode** 可透過 Windows XP Service Pack 2 (SP2) 取得。 它可能在後續版本中無法使用。\]

在視窗中啟用讀取器模式。

## <a name="syntax"></a>語法


```C++
void WINAPI DoReaderMode(
  _In_ PREADERMODEINFO prmi
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*prmi* \[在\]
</dt> <dd>

類型： **PREADERMODEINFO**

[**READERMODEINFO**](readermodeinfo.md)結構的指標，其中包含讀取器模式的初始化資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式不會傳回值。

## <a name="remarks"></a>備註

只要按下滑鼠，就可以透過支援的裝置來啟用讀者模式，通常是使用第三個滑鼠按鍵或滾輪。 在指定區域中的後續滑鼠移動會滾動該區域的內容，而不是移動指標。 在該區域外，滑鼠指標會顯示並正常運作。 第二次按一下按鈕或滾輪會從讀取器模式釋放裝置。

> [!Note]  
> 未在任何公用標頭中宣告此函式。 若要使用它，您必須以 Comctl32.dll 的序數383形式存取它。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista、Windows Vista \[ 桌面應用程式\]<br/>                                                   |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                            |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (4.72 版或更新版本) </dt> </dl> |



 

 





