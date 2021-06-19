---
title: 'Top 屬性 (字元物件) '
description: 深入瞭解 Top property (字元物件) 。 Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a5e26d2ef578a98447d47eb2a3fae3613760a9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396343"
---
# <a name="top-property-characters-object"></a>Top 屬性 (字元物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定指定之字元框架的上邊緣。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 ( "**_CharacterID_*_" ) 的字元。Top_ *  \[  =  *值*\]



| 部分    | 描述                                             |
|---------|---------------------------------------------------------|
| *value* | 指定字元上邊緣的長整數。 |



 

</dd> </dl>

## <a name="remarks"></a>備註

**Top** 屬性一律以圖元表示，相對於螢幕原點 (左上) 。 這個屬性的設定會套用到字元的所有用戶端。

雖然字元會出現在不規則的形狀區域視窗中，但字元的位置是以使用 Microsoft Agent 字元編輯器來編譯字元時所使用之矩形動畫框架的外部維度為基礎。

使用 [**MoveTo**](moveto-method.md) 方法來變更字元的位置。

## <a name="see-also"></a>另請參閱

[**左屬性**](left-property.md)、 [ **MoveTo 方法**](moveto-method.md)


 

 




