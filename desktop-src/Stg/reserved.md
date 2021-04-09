---
title: 保留
description: DWORD 資料類型的值已保留供日後使用。
ms.assetid: 3b49c064-43d0-4e76-b199-c2f6d1c153d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d791debea3835ec1b2fb1fc9d48df7c92114e44e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840880"
---
# <a name="reserved"></a><span data-ttu-id="645cf-103">保留</span><span class="sxs-lookup"><span data-stu-id="645cf-103">Reserved</span></span>

<span data-ttu-id="645cf-104">**DWORD** 資料類型的值已保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="645cf-104">The value of the **DWORD** data type is reserved for future use.</span></span> <span data-ttu-id="645cf-105">屬性集的寫入器應該將此值設為 1;屬性集的讀取器應確定此值至少為1。</span><span class="sxs-lookup"><span data-stu-id="645cf-105">Writers of property sets should set this value to 1; readers of property sets should ensure that this value is at least 1.</span></span> <span data-ttu-id="645cf-106">此指導方針的例外狀況是，針對 [DocumentSummaryInformation 和使用者配置的屬性集](the-documentsummaryinformation-and-userdefined-property-sets.md)，這個值可能是2。</span><span class="sxs-lookup"><span data-stu-id="645cf-106">An exception to this guideline is that, for [The DocumentSummaryInformation and UserDefined Property Sets](the-documentsummaryinformation-and-userdefined-property-sets.md), this value may be 2.</span></span>

 

 




