---
title: 書簽事件
description: 書簽事件
ms.assetid: 6733cd4e-2ba0-4cff-b68d-abfea284f748
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0695ccd04f93eae46eaae66955c84fefb9e0c963
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183343"
---
# <a name="bookmark-event"></a>書簽事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

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

 

 




