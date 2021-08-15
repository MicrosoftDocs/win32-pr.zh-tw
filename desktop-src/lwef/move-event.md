---
title: 移動事件
description: 移動事件
ms.assetid: 973e9e68-edbb-4741-b50e-57db96712df8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9938f79a0c23340c5ed34be52019afe5f9f3fa6caefb6920941cb17dc13c0fc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476346"
---
# <a name="move-event"></a>移動事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

移動字元時發生。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

**子***代理程式* \_ **移動 (byval** *CharacterID*， **byval** *X*， **byval** *Y*， **byval** *原因 * * * )**



| 部分          | 描述                                                                                                                                                                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | 傳回已移動之字元的識別碼。                                                                                                                                                                                                                                                                                                   |
| *X*           | 以圖元為單位，傳回字元框架新位置上邊緣的 x 座標 (（以圖元為單位) ）。                                                                                                                                                                                                                                         |
| *Y*           | 以圖元為單位，傳回字元框架的新位置左邊緣的 y 座標 (（以圖元為單位) ）。                                                                                                                                                                                                                                        |
| *原因*       | 傳回值，這個值會指出造成字元移動的原因。 1使用者拖曳字元。<br/> 2您的用戶端應用程式移動字元。<br/> 3其他用戶端應用程式移動字元。<br/> 4代理程式伺服器移動字元，以在螢幕解析度變更之後讓它保持在畫面上。<br/> |



 

</dd> </dl>

### <a name="remarks"></a>備註

當使用者或應用程式變更字元的位置時，就會發生此事件。 座標與畫面的左上角有關。 此事件只會傳送給已載入字元)  (應用程式的字元用戶端。

**另請參閱**

[**MoveCause 屬性**](movecause-property.md)， [**大小事件**](size-event.md)

 

 





