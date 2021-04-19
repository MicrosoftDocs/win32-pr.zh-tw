---
description: 提供者特定的對話方塊函式可讓提供者藉由變更系統對話方塊或顯示自訂對話方塊，來顯示及處理網路特定的資訊。
ms.assetid: c9a52867-0a0b-40d8-a09d-2b7bed517e13
title: Provider-Specific 對話方塊函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 567c4dcb9f1fd6c2e289d678cf09b3d0d66e4207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980614"
---
# <a name="provider-specific-dialog-box-functions"></a>Provider-Specific 對話方塊函數

提供者特定的對話方塊函式可讓提供者藉由變更系統對話方塊或顯示自訂對話方塊，來顯示及處理網路特定的資訊。

下列對話方塊功能會將按鈕新增至 [檔案管理員 **屬性** ] 對話方塊。 然後，提供者可以處理這些按鈕的事件，以執行網路特定的工作。 請注意，可加入的按鈕數目有限制。 因此，提供者應該謹慎使用這項功能。 此外，提供者可能會發現自己無法加入按鈕，因為其他提供者已經使用了可用的空間。 網路提供者應該會處理這種情況。



| 函式                                           | 描述                                                                                                                             |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext)     | 決定針對特定資源新增至屬性對話方塊的按鈕名稱。<br/>                                      |
| [**NPPropertyDialog**](/windows/desktop/api/Npapi/nf-npapi-nppropertydialog)       | 當使用者按一下使用 [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) 函式加入的按鈕時呼叫。<br/>               |
| [**NPSearchDialog**](/windows/desktop/api/Npapi/nf-npapi-npsearchdialog)           | 可讓網路提供者在 **連接** 對話方塊中所提供的以外，執行自己的搜尋功能。<br/> |
| [**NPFormatNetworkName**](/windows/desktop/api/Npapi/nf-npapi-npformatnetworkname) | 可讓網路提供者在將網路名稱呈現給使用者之前，先將其格式化或修改。<br/>                 |



 

 

 




