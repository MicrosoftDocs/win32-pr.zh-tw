---
title: 顯示事件
description: 顯示事件
ms.assetid: vs|msagent|~\pacontrol_7wrw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b126c7726f8b8ed3ce1e83162cf41ad3223700630167448ff8a7655817a0604
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975736"
---
# <a name="show-event"></a>顯示事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

發生于顯示字元時。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

**子***代理程式 * * * \_ 顯示 (byval* *  *CharacterID*， **byval** *原因 * * * )**



| 部分          | 描述                                                                                                                                                                                                                                                                 |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | 傳回顯示為字串之字元的識別碼。                                                                                                                                                                                                                          |
| *原因*       | 傳回值，這個值會指出造成字元顯示的原因。 2使用者使用功能表或語音命令) 顯示字元 (。<br/> 4您的用戶端應用程式會顯示該字元。<br/> 6另一個用戶端應用程式顯示該字元。<br/> |



 

</dd> </dl>

### <a name="remarks"></a>備註

伺服器會將此事件傳送給該字元的所有用戶端。 若要查詢字元的目前狀態，請使用 [**Visible**](visible-property.md) 屬性。

### <a name="see-also"></a>另請參閱

[**隱藏事件**](hide-event.md)， [ **VisibilityCause**](visibilitycause-property.md)


 

 





