---
title: 寫入檔案
description: 寫入檔案
ms.assetid: a01f93e9-e0fe-4e81-aa9f-62cdca7bce4a
keywords:
- AVIFileWriteData 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7bf46125d9da8b9e5e0668f504028db8b011c99c780b545f9ea99accc0a9ecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891768"
---
# <a name="writing-to-a-file"></a>寫入檔案

您可以使用 [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) 函式，將補充資訊寫入已使用寫入權限開啟的檔案。 此函式會從應用程式提供的緩衝區複製資訊，並將其放入檔案中的一或多個區塊。 "INFO" 區塊是一種常見的 RIFF 區塊類型，其中函數會儲存補充資訊。 如需 RIFF 檔及其資料區塊的說明，請參閱 [資源交換檔案格式服務](resource-interchange-file-format-services.md)。

 

 




