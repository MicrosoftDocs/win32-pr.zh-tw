---
description: 當應用程式使用認證管理 API 提示輸入認證時，使用者應該輸入可由作業系統或應用程式驗證的資訊。
ms.assetid: 53ed2eb4-2c29-48fd-b7fa-0c27bf155758
title: 使用者名稱格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fb99a9e6064cd3883a8d71c1e76ca853d88661
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980582"
---
# <a name="user-name-formats"></a>使用者名稱格式

當應用程式使用認證管理 API 提示輸入認證時，使用者應該輸入可由作業系統或應用程式驗證的資訊。 使用者可以使用下列其中一種格式來指定網域認證資訊：

-   [使用者主體名稱](#user-principal-name)
-   [下層登入名稱](#down-level-logon-name)

## <a name="user-principal-name"></a>使用者主體名稱

[*使用者主體名稱*](../secgloss/u-gly.md) (UPN) 格式是用來指定網際網路樣式的名稱，例如 <b>UserName@Example.Microsoft.com</b> 。 下表摘要說明 UPN 的各部分。



| 部分                                                        | 範例                                |
|-------------------------------------------------------------|----------------------------------------|
| 使用者帳戶名稱。 也稱為登入名稱。<br/> | *使用者名稱*<br/>                  |
| 分隔符號。 字元常值，@ 符號 ( @ ) 。<br/> | @<br/>                           |
| UPN 尾碼。 也稱為功能變數名稱。<br/>       | *Example.Microsoft.com* <br/> |



 

UPN 可以隱含或明確定義。 隱含 UPN 的格式為 <b>UserName@DNSDomainName.com</b> 。 即使未定義明確的 UPN，隱含的 UPN 一律會與使用者的帳戶相關聯。 明確的 UPN 是表單 <i><b>Name@Suffix</b></i> ，系統管理員會明確定義名稱和尾碼字串。

## <a name="down-level-logon-name"></a>Down-Level 登入名稱

下層登入名稱格式是用來指定網域和該網域中的使用者帳戶，例如 <i><b>網域 \\ </b></i>使用者名稱。 下表摘要說明下層登入名稱的各部分。



| 部分                                                           | 範例               |
|----------------------------------------------------------------|-----------------------|
| NetBIOS 功能變數名稱。<br/>                                | *DOMAIN*<br/>   |
| 分隔符號。 字元常值， () 的反斜線 \\ 。<br/> | **\\**<br/>     |
| 使用者帳戶名稱。 也稱為登入名稱。<br/>    | *使用者名稱*<br/> |



 

 

 
