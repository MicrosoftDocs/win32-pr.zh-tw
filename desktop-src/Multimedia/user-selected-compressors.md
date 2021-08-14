---
title: User-Selected 壓縮機
description: User-Selected 壓縮機
ms.assetid: 38569f9c-2df3-4959-990b-5c33203ff916
keywords:
- 影片壓縮管理員 (BC-VCM-LVM-HYPERV) ，使用者選取的壓縮機
- BC-VCM-LVM-HYPERV (video 壓縮管理員) ，使用者選取的壓縮機
- ICCompressorChoose 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c855acb1ecd69876009d0cc3eb6a3b3f4129cc252183e40c5b2d00289be82842
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370798"
---
# <a name="user-selected-compressors"></a>User-Selected 壓縮機

壓縮資料時，您的應用程式可以使用 [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) 函式來建立對話方塊，讓使用者可以在其中選取壓縮程式。 您可以指定此函式的旗標，讓使用者指定主要畫面格頻率和電影資料速率，或顯示預覽視窗。

系統會自動開啟使用者所選取的壓縮程式，並在 **ICCompressorChoose** 中指定之 [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars)結構的 .hic .hid 成員傳回其控制碼。

如果您使用 **ICCompressorChoose**，請使用 [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) 函式來關閉壓縮功能，並釋放與 **COMPVARS** 結構相關聯的任何資源。

 

 




