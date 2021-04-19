---
description: HTAPILINE 資料類型代表行資料結構的 TAPI 不透明控制碼。
ms.assetid: 732f0990-cbad-4ce0-873f-7b025603466e
title: HTAPILINE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80da6db2364b98647e542ece4b71aafd03f4fd9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993003"
---
# <a name="htapiline"></a><span data-ttu-id="eb7f7-103">HTAPILINE</span><span class="sxs-lookup"><span data-stu-id="eb7f7-103">HTAPILINE</span></span>

<span data-ttu-id="eb7f7-104">**HTAPILINE** 資料類型代表行資料結構的 TAPI 不透明控制碼。</span><span class="sxs-lookup"><span data-stu-id="eb7f7-104">The **HTAPILINE** datatype represents the TAPI opaque handle for a line data structure.</span></span> <span data-ttu-id="eb7f7-105">TAPI 必須將此類型的值解析為適當資料結構實例的參考。</span><span class="sxs-lookup"><span data-stu-id="eb7f7-105">TAPI must resolve a value of this type into a reference to the appropriate data structure instance.</span></span> <span data-ttu-id="eb7f7-106">服務提供者不得嘗試透過這個方式來參考它，就像它是指標、對其值進行假設，或是以任何方式解讀其標記法，而不是在適當的時間將其值傳遞給 TAPI。</span><span class="sxs-lookup"><span data-stu-id="eb7f7-106">The service provider must not attempt to reference through this as if it were a pointer, make assumptions about its values, or interpret its representation in any way other than passing its value to TAPI at appropriate times.</span></span>

 

 



