---
description: FormatProperties 匯出函式會格式化網路監視器 UI 的詳細資料窗格中所顯示的資料。 如果您想要在 [詳細資料] 窗格中顯示資料，您必須在所有剖析器 Dll 中執行 FormatProperties export 函數。
ms.assetid: 78e0b4b9-f19e-41cb-8504-635f3f9ac1ee
title: 'FormatProperties 回呼函數 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 61707b49fa88490e1aa22ac89f33dfd97ec20cbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972375"
---
# <a name="formatproperties-callback-function"></a>FormatProperties 回呼函式

**FormatProperties** 匯出函式會格式化網路監視器 UI 的詳細資料窗格中所顯示的資料。 如果您想要在 [詳細資料] 窗格中顯示資料，您必須在所有剖析器 Dll 中執行 **FormatProperties** export 函數。

## <a name="syntax"></a>語法


```C++
DWORD FormatProperties(
  _In_ HFRAME         hFrame,
  _In_ LPBYTE         lpFrame,
  _In_ LPBYTE         lpProtocol,
  _In_ DWORD          nPropertyInsts,
  _In_ LPPROPERTYINST lpPropInst
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hFrame* \[在\]
</dt> <dd>

要剖析之框架的控制碼。

</dd> <dt>

*lpFrame* \[在\]
</dt> <dd>

框架第一個位元組的指標。

</dd> <dt>

*lpProtocol* \[在\]
</dt> <dd>

框架中通訊協定資料開頭的指標。

</dd> <dt>

*nPropertyInsts* \[在\]
</dt> <dd>

*LpPropInst* 所提供的 [PROPERTYINST](propertyinst.md)結構數目。

</dd> <dt>

*lpPropInst* \[在\]
</dt> <dd>

[PROPERTYINST](propertyinst.md)結構陣列的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 **TRUE**。

如果函式不成功，則傳回值為 **FALSE**。

## <a name="remarks"></a>備註

網路監視器會呼叫 **FormatProperties** 函式，以便在網路監視器 UI 的詳細資料窗格中顯示資料。 一般來說，會呼叫 **FormatProperties** 來格式化通訊協定的摘要行，然後格式化框架內的所有通訊協定屬性實例。 不過，網路監視器不保證它針對特定剖析器呼叫 **FormatProperties** 的次數。

在 **FormatProperties** 函式的執行期間，剖析器會間接呼叫 [FormatPropertyInstance](formatpropertyinstance.md) 函式，以使用網路監視器提供的一般格式器，或呼叫剖析器所定義的自訂格式器程式。 您必須針對傳遞給 *lpPropInst* 參數中剖析器 DLL 的每個 [PROPERTYINST](propertyinst.md)結構，呼叫其中一個格式器。



| 的相關資訊                                          | 請參閱                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| 什麼是剖析器，以及它們如何搭配網路監視器運作。   | [解析 器](parsers.md)                                             |
| 剖析器 DLL 中包含的進入點。          | [剖析器 DLL 架構](parser-dll-architecture.md)             |
| 如何執行 **FormatProperties**  包含範例。 | [執行 FormatProperties](implementing-formatproperties.md) |
| 一般格式器如何格式化不同類型的資料。  | [一般格式器輸出](generic-formatter-output.md)           |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[FormatPropertyInstance](formatpropertyinstance.md)
</dt> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> <dt>

[PROPERTYINST](propertyinst.md)
</dt> </dl>

 

 




