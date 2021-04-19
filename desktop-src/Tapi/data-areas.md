---
description: 某些電話組支援將資料從資料下載或上傳至電話裝置的概念，可讓您以各種方式將電話設定為程式設計。
ms.assetid: 5734107d-8104-4d8a-b3f7-3cc2a48f71ca
title: 資料區域
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81376549c63b4fcea92f705246cd58161faeac94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975084"
---
# <a name="data-areas"></a>資料區域

某些電話組支援將資料從資料下載或上傳至電話裝置的概念，可讓您以各種方式將電話設定為程式設計。 TAPI 會將這些電話設定為具有一或多個下載或上傳區域的模型。 每個區域都是由數位所識別，其範圍從零到電話上可用的資料區域數目減一。 每個區域的大小可能各不相同。 資料本身的格式是裝置特定的。

TAPI [**phoneSetData**](/windows/desktop/api/Tapi/nf-tapi-phonesetdata) 函式會將資料緩衝區下載至電話裝置中的指定資料區域，而 [**phoneGetData**](/windows/desktop/api/Tapi/nf-tapi-phonegetdata) 函式會將電話裝置中特定資料區域的內容上傳到緩衝區。

當手機裝置的資料區域變更時，會將 [**電話 \_ 狀態**](phone-state.md) 消息傳送至應用程式，以通知應用程式狀態變更。 此訊息的參數提供了變更的指示。

 

 



