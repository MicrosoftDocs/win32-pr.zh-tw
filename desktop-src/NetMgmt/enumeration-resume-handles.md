---
title: 列舉 Resume 控制碼
description: 列舉 resume 控制碼是函數實例資料中包含之實際 resume 索引鍵的識別碼。 這是安全性和互通性的必要項，可簡化函式的呼叫端程式碼。
ms.assetid: 6734e99b-7f8c-43c9-96e3-44c9783960dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f20e7a7d5e1f9afb15e6adad4c0d7643bf841d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932243"
---
# <a name="enumeration-resume-handles"></a>列舉 Resume 控制碼

列舉 resume 控制碼是函數實例資料中包含之實際 resume 索引鍵的識別碼。 這是安全性和互通性的必要項，可簡化函式的呼叫端程式碼。

如果傳遞給 resume 控制碼的指標的 **Null 是 Null** ，則不會儲存任何控制碼，且列舉搜尋無法繼續。 這在應用程式不想列舉所有專案的情況下很有用。

如果從列舉呼叫傳回錯誤，則必須將 resume 控制碼視為無效，且不會用於任何後續的列舉呼叫。 發生這種情況時，您必須從頭重新開機列舉。

 

 




