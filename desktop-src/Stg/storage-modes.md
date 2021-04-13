---
title: 儲存模式
description: 非同步儲存體支援兩種儲存模式封鎖和非封鎖，用戶端 (瀏覽器或物件本身) 可以藉由 \_ 將 BINDF ASYNCSTORAGE 從標記的呼叫傳回至 IBindStatusCallback GetBindInfo 來指定。
ms.assetid: df8f9e2c-40d2-4997-b5f9-bdbc524437cf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 827e893f5077a64485251111837e6b56657756f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376149"
---
# <a name="storage-modes"></a>儲存模式

非同步存放裝置支援兩種儲存模式：封鎖和非封鎖，用戶端 (瀏覽器或物件本身) 可以藉由將 BINDF \_ ASYNCSTORAGE 從標記的呼叫傳回至 [**IBindStatusCallback：： GetBindInfo**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775058(v=vs.85))來指定。 如果用戶端指定 BINDF \_ ASYNCSTORAGE，則會收到非封鎖的非同步存放裝置指標。 否則，它會收到封鎖非同步儲存的指標。 即使用戶端未向系結內容) 註冊 [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) ，也不會要求非同步系結作業 (，但該標記仍會傳回封鎖的非同步存放裝置，以啟用繼承應用程式的漸進式載入。

在非封鎖模式中，非同步存放裝置 \_ 會在資料無法使用時傳回 E 暫止。 收到此訊息時，用戶端會等待通知，指出有其他資料可供使用，然後再嘗試下載。

在封鎖模式下， \_ 非同步儲存體會封鎖呼叫，直到有新的資料可用，然後解除封鎖呼叫並傳回新的資料，而不是傳回 E 暫止。 用戶端必須準備好接收資料。 當執行緒遭到封鎖時，已傳遞至用戶端的資料會完全提供給使用者。

封鎖模式是必要的，因為不知道非同步存放裝置的用戶端將無法辨識 E \_ 暫止，並會假設發生無法復原的錯誤。 封鎖非同步存放裝置可讓現有的用戶端進行漸進式轉譯。

 

 