---
description: 有兩種類型的追蹤終端機定義錄製追蹤終端機和播放播放軌終端機，分別屬於和管理檔案記錄終端機和檔案播放終端。
ms.assetid: 2c5c485e-d46f-4bfe-8651-5ed021b23b66
title: 追蹤終端機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5bec904b5ae7ac7528c4cf701139e30cc8da05e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984640"
---
# <a name="track-terminals"></a>追蹤終端機

定義了兩種類型的追蹤終端機：錄製追蹤終端機和播放播放軌終端機，分別屬於和都是由檔案記錄終端機和檔案播放終端來管理。

所有追蹤終端機都會公開 [**ITFileTrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack) 和 [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) 介面。 **ITTerminal** 介面允許將追蹤終端機選取到資料流程或呼叫。

> [!Note]  
> 追蹤終端機也會公開由 MSP 使用的私用介面 [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol)。 應用程式不應該嘗試存取這個介面。

 

 

 
