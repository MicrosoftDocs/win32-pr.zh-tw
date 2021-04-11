---
description: TAPI 提供手機顯示器的存取權。
ms.assetid: f6017ecc-b2a0-4a92-8c28-ce7411f8dd84
title: 顯示
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dd813297c1d4624bb37cea8d833f63bcebeeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113192"
---
# <a name="display"></a>顯示

TAPI 提供電話顯示的存取權。 顯示會模型化為具有資料列和資料行的英數位元區域。 手機的裝置功能會將電話的顯示大小指定為數據列數目和資料行數目。 如果手機裝置沒有顯示，這兩個數字都是零。 使用 [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) 將資訊寫入至開啟的電話裝置，並使用 [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) 來取出手機顯示器的目前內容。

當手機裝置的顯示變更時，就會將 [**電話 \_ 狀態**](phone-state.md) 消息傳送至應用程式函式，以通知應用程式狀態變更。 此訊息的參數提供了變更的指示。

 

 



