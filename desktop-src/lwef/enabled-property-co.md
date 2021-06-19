---
title: 'Enabled 屬性 (Command 物件) '
description: 瞭解已啟用的命令物件屬性。 Microsoft Agent 已于 Windows 7 淘汰。
ms.assetid: d9dcbdf0-ba35-4ebd-b6f2-f3c8bdfc0431
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc0c65d5cfa0438fe9d61eac0c59e916731e057
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407331"
---
# <a name="enabled-property-command-object"></a>Enabled 屬性 (Command 物件) 

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

傳回或設定是否在指定的字元快顯功能表中啟用 **命令** 。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

*代理程式 ***。 (**"_CharacterID_*_" ) 的字元 ) 的命令 ( "_*_name_*_"。啟用_ 的 *  \[  =  *布林值*\]



| 部分      | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | 指定是否啟用 **命令** 的布林運算式。<br/> <dl> <dt><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True**</dt> <dd> **命令** 已啟用。<br/> </dd> <dt><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False**</dt> <dd> 此 **命令** 已停用。<br/> </dd> </dl> |



 

</dd> </dl>

## <a name="remarks"></a>備註

如果 [ [**已啟用**](enabled-property.md) ] 屬性設定為 [ **True**]，當用戶端應用程式為輸入-主動時， [**命令**](/windows/desktop/lwef/the-command-object) 物件的標題會顯示為字元快顯功能表中的一般文字。 如果 **Enabled** 屬性為 **False**，標題會顯示為無法使用 (已停用) 文字。 語音輸入也無法存取已停用的 **命令** 。

 

