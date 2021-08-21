---
title: 書簽事件
description: 書簽事件
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c6a6dcd072b87c6a924c8d33e6ebb73c75c927bdf955f51612703d3fc18af79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976708"
---
# <a name="bookmark-event"></a>書簽事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

發生于已啟用您的應用程式所定義之語音文字字串中的書簽時。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

**子***代理程式* \_ **書簽** **(ByVal** *BookmarkID * * * )**



| 部分         | 描述                                     |
|--------------|-------------------------------------------------|
| *BookmarkID* | 識別書簽編號的長整數。 |



 

</dd> </dl>

### <a name="remarks"></a>備註

若要指定書簽事件，請在提供的文字中使用 [**說話**](speak-method.md) 方法與 **Mrk** 標記。 如需標記的詳細資訊，請參閱語音輸出標記。

 

 




