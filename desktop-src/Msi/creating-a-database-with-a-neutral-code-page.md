---
description: 處理字碼頁的建議方法是撰寫一個中立的基底資料庫，其中只包含可轉譯成任何字碼頁的字元。
ms.assetid: 8ded41a6-6e5b-4a39-b783-e2b9f83eaed4
title: 使用中性字碼頁建立資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08639b6ab3521f183a2dab46dfd257121b28bae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026892"
---
# <a name="creating-a-database-with-a-neutral-code-page"></a>使用中性字碼頁建立資料庫

處理字碼頁的建議方法是撰寫一個中立的基底資料庫，其中只包含可轉譯成任何字碼頁的字元。 然後，資料庫可以設定為當地語系化的字碼頁，而當地語系化資訊可以依照當地語系化 [Windows Installer 套件](localizing-a-windows-installer-package.md)中所述的方式加入。

若要撰寫中性資料庫，請避免不屬於 ASCII 字元集的擴充字元，因此需要特殊字碼頁。 例如，著作權符號、©和註冊的商標符號、不是 ASCII 字元，且需要特殊的 ANSI 字碼頁才能正確顯示。 改為使用 (c) 和 (r) ，因為這些字元可以轉譯或轉換成英文版的符號。 然後，您可以藉由設定其字碼頁，並藉由編輯資料表或匯入文字封存檔案，來將這個中性資料庫當地語系化。

 

 



