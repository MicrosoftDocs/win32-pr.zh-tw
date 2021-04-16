---
title: 用戶端看到的內容
description: 本主題列出用戶端查看 ADSI 資料的方式。
ms.assetid: 238eeea9-1303-4d37-bf09-ad03f1790c1b
ms.tgt_platform: multiple
keywords:
- 擴充功能 ADSI，用戶端看到的內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398c9fd2d603c1eebb18280c435bec7cb7cd8e14
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104508128"
---
# <a name="what-does-a-client-see"></a><span data-ttu-id="2d686-104">用戶端會看到什麼？</span><span class="sxs-lookup"><span data-stu-id="2d686-104">What Does a Client See?</span></span>

-   <span data-ttu-id="2d686-105">用戶端會看到 ADSI 及其所有的擴充物件，做為一個物件。</span><span class="sxs-lookup"><span data-stu-id="2d686-105">A client sees ADSI and all of its extension objects as one object.</span></span>
-   <span data-ttu-id="2d686-106">ADSI 用戶端會看到一個 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面，此介面會處理物件中的所有雙重和分派介面，無論是由提供者中的匯總工具或由擴充功能來執行雙或分派介面。</span><span class="sxs-lookup"><span data-stu-id="2d686-106">An ADSI client sees one [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface that handles all the dual and dispatch interfaces in the object, whether the dual or dispatch interface is implemented by the aggregator in the provider or by an extension.</span></span> <span data-ttu-id="2d686-107">請參閱 [擴充功能中自動化的函式/屬性名稱衝突解決方法](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md)。</span><span class="sxs-lookup"><span data-stu-id="2d686-107">Please see [Resolution of Function/Property Name Conflicts in Automation in Extensions](resolution-of-functionproperty-name-conflicts-in-automation-in-extensions.md).</span></span>
-   <span data-ttu-id="2d686-108">ADSI 不會透過 [**idispatch：： GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) 或 [**Idispatch：： GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) 方法公開任何類型資訊。</span><span class="sxs-lookup"><span data-stu-id="2d686-108">ADSI does not expose any type information through the [**IDispatch::GetTypeInfo**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfo) or [**IDispatch::GetTypeInfoCount**](/windows/win32/api/oaidl/nf-oaidl-idispatch-gettypeinfocount) methods.</span></span> <span data-ttu-id="2d686-109">ADSI 會透過型別程式庫提供型別資訊。</span><span class="sxs-lookup"><span data-stu-id="2d686-109">ADSI provides type information through the type library.</span></span>

 

 