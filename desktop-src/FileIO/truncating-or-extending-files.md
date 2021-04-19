---
description: 應用程式可以藉由呼叫 SetEndOfFile 來截斷或擴充檔案。
ms.assetid: 23a0242d-50e9-4324-bb09-505afe383a80
title: 截斷或擴充檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daf8a2d4e7e346bfea41285be97d6d756e2a6b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978095"
---
# <a name="truncating-or-extending-files"></a>截斷或擴充檔案

應用程式可以藉由呼叫 [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)來截斷或擴充檔案。 此函式會將檔案結尾標記設定為檔案指標的目前位置。

請注意，當擴充檔案時，不會定義舊檔案和新的檔案結尾位置之間的內容。

 

 



