---
title: MCIAVI
description: MCIAVI
ms.assetid: 68639f35-bc20-457d-b937-760af8323dce
keywords:
- MCI 裝置、MCIAVI 驅動程式
- MCI 命令，MCIAVI 驅動程式
- MCIAVI 驅動程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be2e69cf2b0fd9ee71650c56b0d7d9efb50a46e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462321"
---
# <a name="mciavi"></a>MCIAVI

AVI 檔案可以包含兩個以上的資料流程，例如影片順序、英文的聲帶和法文的聲帶。 您的應用程式可以使用與檔案中其他資料流程無關的資料流程。

**Digitalvideo** 裝置類型會控制影片檔案。 如需數位視訊裝置可辨識的 MCI 命令清單，請參閱 [數位視訊命令集](digital-video-command-set.md)。

MCIAVI 驅動程式會在 MCI 命令的控制權下播放影片順序和其他資料流程。 資料流程可以包含影像、音訊和調色板。 影像資料可由具有調色板或真色彩資訊的影像所組成。

音訊會在一秒的 thirtieth 內與影片進行同步處理。 但是，如果無法使用音訊硬體，驅動程式只會播放影片串流。 如有必要，MCIAVI 驅動程式可以卸載影片畫面，以播放資料流程，而不會中斷音訊。

您的應用程式可以使用 MCIWnd 視窗類別服務，而不是使用 MCI 命令介面來控制任何 MCI 驅動程式。 此視窗類別會處理管理支援 MCI 裝置之視窗的許多詳細資料，並簡化傳送 MCI 命令所需的程式設計。 您的應用程式可以直接使用 MCIWnd 程式庫服務來控制 MCI 裝置，也可以讓 MCIWnd 顯示工具列、捲軸和功能表，讓使用者控制裝置。 如需 MCIWnd 視窗類別的詳細資訊，請參閱 [MCIWnd 視窗類別](mciwnd-window-class.md)。

 

 




