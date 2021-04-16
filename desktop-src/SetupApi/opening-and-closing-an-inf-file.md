---
description: 在設定函數可以存取 INF 中的資訊之前，您必須使用 SetupOpenInfFile 函式的呼叫來開啟它。 此函數會傳回 INF 檔案的控制碼。
ms.assetid: d838c05c-51e4-49a8-b773-af4924bff7e2
title: 開啟和關閉 INF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893b72d000f433fb4da7ecfee0db4d856f878814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513544"
---
# <a name="opening-and-closing-an-inf-file"></a>開啟和關閉 INF 檔案

在設定函數可以存取 INF 中的資訊之前，您必須使用 [**SetupOpenInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopeninffilea) 函式的呼叫來開啟它。 此函數會傳回 INF 檔案的控制碼。

如果您不知道需要開啟的 INF 檔案名，可以使用 [**SetupGetInfFileList**](/windows/desktop/api/Setupapi/nf-setupapi-setupgetinffilelista) 函式來取得目錄中的 inf 檔案清單。

開啟 INF 檔案之後，您可以使用 [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) 函式，將其他 INF 檔案附加至已開啟的 inf 檔案。 這項功能類似于 include 語句。 當後續安裝函式參考開放式 INF 檔案時，也可以存取儲存在附加檔案中的任何資訊。

如果您未在 [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea)函式的呼叫期間指定 INF 檔案， **SetupOpenAppendInfFile** 會在 open INF 檔案的 [**版本**] 區段中，將 **LayoutFile** 金鑰所指定的)  (的檔案附加至該檔案。

當您不再需要 INF 檔案中的資訊時，請呼叫 [**SetupCloseInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupcloseinffile) 函式釋放在呼叫 [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea)期間所配置的資源。

 

 



