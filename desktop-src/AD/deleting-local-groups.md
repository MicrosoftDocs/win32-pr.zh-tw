---
title: 刪除本機群組
description: 本主題說明如何從成員伺服器或 Windows 2000 Professional 上執行的電腦刪除本機群組。
ms.assetid: 030da25a-a606-4521-a243-d902c772fd00
ms.tgt_platform: multiple
keywords:
- 刪除本機群組 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe960804e083ecaf8ef12e412a43b7b8db4800f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881478"
---
# <a name="deleting-local-groups"></a>刪除本機群組

本主題說明如何從成員伺服器或 Windows 2000 Professional 上執行的電腦刪除本機群組。

**刪除本機群組**

1.  使用下列規則系結至電腦：
    1.  使用具有足夠許可權的帳戶來存取該電腦。
    2.  使用 WinNT 提供者、電腦名稱稱和額外的參數來使用下列系結字串格式，以指示 ADSI 系結至電腦： "WinNT:// <computer name> ， &lt; computer &gt; "。 「 &lt; 電腦名稱稱」 &gt; 參數是要存取的電腦群組名。 此參數會指示 ADSI 系結至電腦，並允許 WinNT 提供者的剖析器略過一些不明確的解析查詢，以判斷您要系結到的物件類型。
    3.  系結至 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 介面。
2.  使用 [**IADsContainer**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)將 "group" 指定為類別，以刪除群組。

    您不需要呼叫 [**IADs SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) 來認可容器的變更。 [**IADsContainer**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)呼叫會認可將群組直接刪除到目錄中的作業。

 

 
