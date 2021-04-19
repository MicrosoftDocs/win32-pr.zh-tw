---
description: 若要產生對話方塊，提示使用者插入下一個磁片或指定新的來源路徑，請呼叫 SetupPromptForDisk。
ms.assetid: a780e7ab-bd96-43e4-9425-e15a758391f4
title: 提示輸入磁片
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404e88611ec21b7a29d69ab306dc0e7c4e1b98e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982468"
---
# <a name="prompting-for-a-disk"></a>提示輸入磁片

若要產生對話方塊，提示使用者插入下一個磁片或指定新的來源路徑，請呼叫 [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)。 當通知（ [**SPFILENOTIFY \_ NEEDMEDIA**](spfilenotify-needmedia.md)）傳送至回呼常式時，回呼常式會使用這個函式來產生使用者介面。

[**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)所產生的對話方塊可讓使用者選擇插入磁片、指定新的來源路徑，或取消安裝。

您可以使用在呼叫 [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) 期間指定的旗標，來改變對話方塊的配置和行為。 您可以使用這些旗標來控制對話方塊是否包含可讓使用者流覽新來源路徑的按鈕，或略過目前的檔案。 旗標也可讓您控制對話方塊的行為，例如第一次顯示時的嗶聲，以及顯示為前景視窗的功能。

 

 



