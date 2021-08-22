---
title: 不使用磁碟儲存體來捕捉
description: 不使用磁碟儲存體來捕捉
ms.assetid: 2e2f1b67-69be-424c-8a6f-d9db5eeb6088
keywords:
- WM_CAP_SEQUENCE_NOFILE 訊息
- capCaptureSequenceNoFile 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea708bd99cc2c325623eb53d734fadb2acdd0112e3a727fae9bfa741b8d301e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691618"
---
# <a name="capture-without-using-disk-storage"></a>不使用磁碟儲存體來捕捉

您可以使用 [ [**WM \_ CAP \_ 序列 \_ NOFILE**](wm-cap-sequence-nofile.md) 訊息 (或 [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) 宏) ，在不將資料寫入磁片檔案的情況下使用 capture service。 此訊息只適用于搭配可讓您的應用程式直接使用影片和音訊資料的回呼函數。 例如，視訊會議應用程式可能會使用這個訊息來取得串流的影片畫面。 回呼函式會將已捕獲的映射傳送至遠端電腦。

 

 




