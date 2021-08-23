---
title: 頁面屬性
description: 頁面屬性
ms.assetid: c3cf07e9-a324-443b-a0c0-2fb80463548f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ca14a4f68c326d1b231aa106450fefc7607857576f817ffaa255fa27f2249b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601007"
---
# <a name="page-property"></a>頁面屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定顯示在 [Microsoft Agent 屬性工作表] 視窗中的頁面。

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**語法** 
</dt> <dd>

*代理程式 * * *。PropertySheet.Page* *  \[  =  *字串*\]



| 部分     | 描述                                                                                                                                                                                                             |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | 具有下列其中一個值的字串運算式。 **"Speech"** 顯示 [語音輸入] 頁面。<br/> **"Output"** 顯示 [輸出] 頁面。<br/> **"著作權"** 顯示 [著作權] 頁面。<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

如果未安裝任何語音引擎，將 **頁面** 設定為 **"speech"** 沒有任何作用。 此外，視窗的 **Visible** 屬性必須設定為 **True** ，使用者才能看到該頁面。

> [!Note]  
> 使用者可以覆寫這個屬性。

 

 

 





