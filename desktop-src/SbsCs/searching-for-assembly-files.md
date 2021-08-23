---
description: 搜尋元件檔
ms.assetid: 6e6c1104-5cde-4c07-9ee2-d87062675dac
title: 搜尋元件檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b55614278d58913c8fb92371e302ffd71fd28b48b7828351d8ce6b37ae0eddc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884868"
---
# <a name="searching-for-assembly-files"></a>搜尋元件檔

啟用內容可協助載入器尋找元件檔。 當載入器搜尋要依名稱載入的檔案時，它會先搜尋具有指定名稱的檔案，該檔案是由目前作用中啟用內容的成員所參考。 對 [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) 的呼叫也會先找到這些檔案。 具有指定名稱和目前啟用內容的檔案，會在本機目錄或 PATH 環境變數中具有名稱的檔案之前找到並載入。 這表示當您建立資訊清單時，您需要列出所有您打算搭配 **SearchPath**、 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)或靜態匯入使用的檔案。

請注意，使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 或其他未搜尋檔案的函式時，不會自動找到這些檔案。 若要將這些檔案與 **CreateFile** 搭配使用，請先使用 [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) 來尋找隔離檔案的路徑，然後在傳回的路徑上使用 **CreateFile** 。

這種檔案搜尋方法有助於將隔離的應用程式分開，因為具有相同名稱的多個檔案，則只會與不同版本號碼的元件關聯不同。 作業系統可以在檔案作業期間找到正確的檔案。

如果 DLL 使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)以這種方式載入，則會呼叫該 dll 的進入)  (點，而原始啟用內容會保持作用中，但除非 DLL 本身包含特定資源識別碼 (ISOLATIONAWARE \_ 資訊清單 \_ 資源 \_ 識別碼或 2) 

 

 
