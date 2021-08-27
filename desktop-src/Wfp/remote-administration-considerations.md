---
description: 遠端系統管理的系統有一些獨特的考慮。
ms.assetid: bfdf121e-9b4e-4323-82ec-9bd32531caad
title: WFP 遠端系統管理考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b3106a02aa4098d2814a955e6582d6e8f1c79f7f161a6875891e13a0db71a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098588"
---
# <a name="wfp-remote-administration-considerations"></a>WFP 遠端系統管理考慮

遠端系統管理的系統有一些獨特的考慮。 首先，當軟體安裝是使用 SMS 或 MSI) 從遠端部署 (時，[WFP 錯誤] 對話方塊會顯示在本機登入的系統管理員 (（如果有) 的話），而不是安裝服務的螢幕上。 其次，如果系統管理員從遠端登入到終端機伺服器，並安裝取代受保護系統檔案的應用程式，則 [WFP 錯誤] 對話方塊只會顯示在主主控台，而不會顯示在系統管理員的遠端視窗中。

基於這些理由，WFP 會隱藏其錯誤對話方塊，直到系統管理員在本機登入。 遠端系統管理員可以在系統事件記錄檔中找到檔案取代錯誤。

**Windows Vista 和 Windows Server 2008：** 不支援 WFP 遠端系統管理。

 

 



