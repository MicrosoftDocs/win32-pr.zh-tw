---
description: HTAPIPHONE 資料類型代表電話資料結構的 TAPIs 不透明控制碼。
ms.assetid: e869cb3e-0eeb-4edf-a272-a655a236a3a2
title: HTAPIPHONE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94706270b1148166181eda0d8df9b940c269f62a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972480"
---
# <a name="htapiphone"></a><span data-ttu-id="6b9c0-103">HTAPIPHONE</span><span class="sxs-lookup"><span data-stu-id="6b9c0-103">HTAPIPHONE</span></span>

<span data-ttu-id="6b9c0-104">**HTAPIPHONE** 資料類型代表 TAPI 的不透明控制碼，適用于手機資料結構。</span><span class="sxs-lookup"><span data-stu-id="6b9c0-104">The **HTAPIPHONE** datatype represents TAPI's opaque handle for a phone data structure.</span></span> <span data-ttu-id="6b9c0-105">TAPI 必須將此類型的值解析為適當資料結構實例的參考。</span><span class="sxs-lookup"><span data-stu-id="6b9c0-105">TAPI must resolve a value of this type into a reference to the appropriate data structure instance.</span></span> <span data-ttu-id="6b9c0-106">服務提供者不得嘗試透過這個方式來參考它，就像它是指標、對其值進行假設，或是以任何方式解讀其標記法，而不是在適當的時間將其值傳遞給 TAPI。</span><span class="sxs-lookup"><span data-stu-id="6b9c0-106">The service provider must not attempt to reference through this as if it were a pointer, make assumptions about its values, or interpret its representation in any way other than passing its value to TAPI at appropriate times.</span></span>

 

 



