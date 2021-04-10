---
title: RaiseRequestErrors 屬性
description: RaiseRequestErrors 屬性
ms.assetid: 60eb4478-526e-492a-8fb3-d1e54eff9868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9e559f999db663a8a9f5874f6d16a10e1e78ac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104185934"
---
# <a name="raiserequesterrors-property"></a>RaiseRequestErrors 屬性

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定是否引發要求的錯誤。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 * * *。RaiseRequestErrors* *  \[  =  *布林值*\]



| 部分      | 描述                                                                                                                                                                                            |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | 布林值，決定是否引發要求中的錯誤。<br/> **True**    (會引發預設) 要求錯誤。 <br/> **False**     不會引發要求錯誤。<br/> |



 

</dd> </dl>

## <a name="remarks"></a>備註

這個屬性可讓您判斷伺服器是否會在支援 [**要求**](/windows/desktop/lwef/the-request-object) 物件的方法中引發錯誤。 例如，如果您指定的動畫名稱不存在於 [**Play**](play-method.md)方法中，除非您將此屬性設定為 **False**，否則伺服器會引發錯誤 (顯示錯誤訊息) 。

當錯誤引發時，不提供復原的程式設計語言可能很有用。 不過，將此屬性設定為 **False** 時請小心，因為在您的程式碼中找出錯誤可能比較困難。

 

