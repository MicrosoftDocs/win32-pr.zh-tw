---
description: 將新的 IInkStrokeDisp 物件加入至傳入的 InkDivider 物件。
ms.assetid: d5b82244-68d5-4137-aaf4-d3232f7c0779
title: AddOneStroke 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddOneStroke
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0af3913f2579363afbb0c3985ad0f40f58051eac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468585"
---
# <a name="addonestroke-function"></a>AddOneStroke 函式

將新的 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件加入至傳入的 [**InkDivider**](inkdivider-class.md) 物件。

此函式不適合應用程式程式碼使用。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI AddOneStroke(
  _In_ INT_PTR hDivider,
  _In_ int     strokeId,
  _In_ int     cPoints,
  _In_ POINT   *aPoints
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hDivider* \[在\]
</dt> <dd>

[**InkDivider**](inkdivider-class.md)物件的控制碼。

</dd> <dt>

*strokeId* \[在\]
</dt> <dd>

要加入至 [**InkDivider**](inkdivider-class.md)物件之 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件的 [**識別碼**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id)。

</dd> <dt>

*cPoints* \[在\]
</dt> <dd>

組成新 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件的封包數目。

</dd> <dt>

*aPoints* \[在\]
</dt> <dd>

組成 *strokeId* 中 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件的封包陣列。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函數可以傳回其中一個值。



| 傳回碼                                                                                  | Description                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此函數已成功。<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *HDivider* 參數無效。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                             |
| 程式庫<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




