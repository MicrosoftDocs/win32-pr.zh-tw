---
description: Winternl .h 標頭檔會公開內部 Windows Api 的原型。 沒有相關聯的匯入程式庫，因此開發人員必須使用執行時間動態連結來呼叫此標頭檔中所述的函式。
ms.assetid: 11f09479-e04b-4e5e-bc46-a2d0daf13785
title: 呼叫內部 Api
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a8ad3533db411d6143d64ca0f4c559334ccaaa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936238"
---
# <a name="calling-internal-apis"></a>呼叫內部 Api

Winternl .h 標頭檔會公開內部 Windows Api 的原型。 沒有相關聯的匯入程式庫，因此開發人員必須使用執行時間動態連結來呼叫此標頭檔中所述的函式。

Winternl 中的函式和結構是作業系統內部的函式和結構，而且可能會從某個 Windows 版本變更為下一個版本，而且可能甚至是每個版本的 service pack 之間的變更。 為了維持應用程式的相容性，您應該改為使用對等的公用函數。 您可以在標頭檔、Winternl 和每個函式的檔中找到進一步的資訊。

如果您使用這些函式，您可以透過使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)的執行時間動態連結來存取這些函數。 這可讓您的程式碼有機會在作業系統中的函式已變更或移除時正常回應。 不過，簽章變更可能無法偵測。

 

 
