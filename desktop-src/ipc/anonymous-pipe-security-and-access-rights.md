---
description: 當您呼叫 CreatePipe 函式時，可以指定匿名管道的安全描述項。 安全描述項可控制對管道的讀取和寫入端的存取。
ms.assetid: 17813ce1-b3f6-408f-9c55-5caa7eda6738
title: 匿名管道安全性和存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02935a3b2bc5ea31d88aab3f23f23c348c054e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978150"
---
# <a name="anonymous-pipe-security-and-access-rights"></a>匿名管道安全性和存取權限

Windows 安全性可讓您控制匿名管道的存取。 如需安全性的詳細資訊，請參閱 [存取控制模型](/windows/desktop/SecAuthZ/access-control-model)。

當您呼叫 [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)函式時，可以指定管道的 [安全描述項](/windows/desktop/SecAuthZ/security-descriptors)。 安全描述項可控制對管道的讀取和寫入端的存取。 如果您指定 **Null**，管道會取得預設安全描述項。 管道之預設安全描述項中的 Acl 來自于建立者的主要或模擬權杖。

若要取出管道的安全描述項，請呼叫 [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) 函數。 若要變更管道的安全描述項，請呼叫 [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) 函數。

[**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)函式會將兩個控制碼傳回給匿名管道：具有泛型 \_ 讀取和同步存取的讀取控制碼; 以及具有一般 \_ 寫入和同步存取的寫入控制碼。 一般 \_ 讀取和一般 \_ 寫入存取會使用與具名管道相同的存取權限對應。

\_匿名管道的一般讀取存取結合了從管道讀取資料、讀取管道屬性、讀取擴充屬性，以及讀取管線的 DACL 的許可權。

\_匿名管道的一般寫入存取結合了將資料寫入管道的許可權、將資料附加至管線、寫入管道屬性、寫入擴充屬性，以及讀取管線的 DACL。

 

 
