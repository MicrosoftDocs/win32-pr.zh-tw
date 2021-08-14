---
title: SAM RPC 通訊協定的遠端呼叫僅限於本機系統管理員
description: SAM RPC 通訊協定受到限制。 這表示只有本機系統管理員群組的成員可以對此通訊協定中的方法進行遠端呼叫。 Active Directory 網域控制站的行為不會受到影響。
ms.assetid: 816BFB8C-A8EE-44F4-864D-748AF8BCF1F8
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee009e3f346c7e7a179a324ec68834999acd711934ab5c64a3cae1845372dbdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211333"
---
# <a name="remote-calls-to-the-sam-rpc-protocol-are-restricted-to-only-local-administrators"></a>SAM RPC 通訊協定的遠端呼叫僅限於本機系統管理員

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

SAM RPC 通訊協定受到限制。 這表示只有本機系統管理員群組的成員可以對此通訊協定中的方法進行遠端呼叫。 Active Directory 網域控制站的行為不會受到影響。

## <a name="mitigations"></a>風險降低

確定已將正確的使用者設定為電腦上的系統管理員。 用於存取檢查的 ACL 可透過群組原則來設定。

 

 




