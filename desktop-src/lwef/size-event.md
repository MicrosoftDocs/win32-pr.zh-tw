---
title: 大小事件
description: 大小事件
ms.assetid: 06089f84-8e75-475f-a492-536c83fa6730
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9a896d2dcbf8b925c0ca13fa429f6dfd95bc21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839867"
---
# <a name="size-event"></a>大小事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

發生于字元的大小變更時。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

**子***代理程式* \_ **大小 (byval** *CharacterID*， **byval** *寬度*， **byval** *高度*) 



| 部分          | 描述                                                         |
|---------------|---------------------------------------------------------------------|
| *CharacterID* | 傳回已移動之字元的識別碼。                         |
| *寬度*       | 傳回字元框架的新寬度 (以圖元為單位) 為整數。  |
| *高度*      | 傳回字元框架的新高度 (以圖元為單位) 為整數。 |



 

</dd> </dl>

### <a name="remarks"></a>備註

當應用程式變更字元的大小時，就會發生此事件。 此事件只會傳送給已載入字元)  (應用程式的字元用戶端。

### <a name="see-also"></a>另請參閱

[**移動事件**](move-event.md)


 

 




