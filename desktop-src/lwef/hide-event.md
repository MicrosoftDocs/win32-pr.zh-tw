---
title: 隱藏事件
description: 隱藏事件
ms.assetid: vs|msagent|~\pacontrol_9yuk.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02974d1d66a22eab24c93fc5c9d29b9c2d0e604082fef9f4f0583ebcf7354576
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062058"
---
# <a name="hide-event"></a>隱藏事件

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

發生于隱藏字元時。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

**子***代理程式 * * * \_ 隱藏 (* *  **byval** *CharacterID*， **byval** *原因 * * * )**



| 部分          | 描述                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | 以字串形式傳回隱藏字元的識別碼。                                                                                                                                                                                                                                                                                                                                                               |
| *原因*       | 傳回值，這個值會指出造成字元隱藏的原因。 1使用者藉由在字元的工作列圖示快顯功能表上選取命令，或使用語音輸入，來將字元隱藏起來。<br/> 3您的用戶端應用程式會將字元隱藏。<br/> 5另一個用戶端應用程式會將字元隱藏。<br/> 7使用者在字元的快顯功能表上選取命令以隱藏字元。<br/> |



 

</dd> </dl>

### <a name="remarks"></a>備註

伺服器會將此事件傳送給該字元的所有用戶端。 若要查詢字元的目前狀態，請使用 [**Visible**](visible-property.md) 屬性。

### <a name="see-also"></a>另請參閱

[**顯示事件**](show-event.md)， [ **VisibilityCause**](visibilitycause-property.md)


 

 





