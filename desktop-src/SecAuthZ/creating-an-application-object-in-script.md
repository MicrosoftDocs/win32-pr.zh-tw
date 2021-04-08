---
description: 針對使用授權原則存放區的每個應用程式，您必須建立 IAzApplication 物件，然後將它儲存至原則存放區。
ms.assetid: 5df964de-e5b6-427e-b859-efb5866f1578
title: 在腳本中建立應用程式物件
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a4852ef0c06d721f9409c000989895f6767eb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691424"
---
# <a name="creating-an-application-object-in-script"></a>在腳本中建立應用程式物件

授權原則存放區包含一或多個應用程式的授權原則資訊。 針對使用授權原則存放區的每個應用程式，您必須建立 [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) 物件，並將它儲存至原則存放區。

下列範例示範如何建立代表應用程式的 [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) 物件，以及如何將 **IAzApplication** 物件加入至應用程式所使用的授權原則存放區。 此範例假設在磁片磁碟機 C 的根目錄中有一個名為 MyStore.xml 的現有 XML 原則存放區。


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.CreateApplication("Expense")

'  Save changes to the store.
expenseApp.Submit
```



 

 



