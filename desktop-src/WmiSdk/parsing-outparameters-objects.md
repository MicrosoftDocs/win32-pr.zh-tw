---
description: SWbemMethod. OutParameters 物件是由執行的提供者方法所建立並提供資料。
ms.assetid: fc06d6a1-770a-4f34-affd-f5035dad9360
ms.tgt_platform: multiple
title: 剖析 OutParameters 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ae3c5d57e9984fceef55de278ed92eba520
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320535"
---
# <a name="parsing-outparameters-objects"></a><span data-ttu-id="29be4-103">剖析 OutParameters 物件</span><span class="sxs-lookup"><span data-stu-id="29be4-103">Parsing OutParameters Objects</span></span>

<span data-ttu-id="29be4-104">[**SWbemMethod. OutParameters**](swbemmethod-outparameters.md)物件是由執行的提供者方法所建立並提供資料。</span><span class="sxs-lookup"><span data-stu-id="29be4-104">A [**SWbemMethod.OutParameters**](swbemmethod-outparameters.md) object is created and supplied with data by the provider method that is executing.</span></span> <span data-ttu-id="29be4-105">**OutParameters** 物件的屬性是所呼叫方法的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="29be4-105">Properties of the **OutParameters** object are specific to the method called.</span></span> <span data-ttu-id="29be4-106">例如，在下列腳本中， *outParam*) 中所包含的 *SD* (是針對 **\_ \_ SystemSecurity. GetSD** 方法定義的 output 參數。</span><span class="sxs-lookup"><span data-stu-id="29be4-106">For example, in the script below, *SD* (contained in *outParam*) is the output parameter defined for the **\_\_SystemSecurity.GetSD** method.</span></span> <span data-ttu-id="29be4-107">**ReturnValue** 屬性是包含作業結果之所有 **OutParameters** 物件的可用泛型屬性。</span><span class="sxs-lookup"><span data-stu-id="29be4-107">The **ReturnValue** property is a generic property available for all **OutParameters** objects which contain the result of the operation.</span></span>

<span data-ttu-id="29be4-108">下列程式碼範例說明如何從本機系統的類別 [**\_ \_ SystemSecurity**](--systemsecurity.md)中執行 [**GetSD**](--systemsecurity-getsd.md)方法，以取得輸出參數。</span><span class="sxs-lookup"><span data-stu-id="29be4-108">The following code example illustrates obtaining output parameters from executing the [**GetSD**](--systemsecurity-getsd.md) method in class [**\_\_SystemSecurity**](--systemsecurity.md) for the local system.</span></span>


```VB
' Connect to WMI root\cimv2 namespace.
Set svc = GetObject("winmgmts:root/cimv2")
' Execute the GetSD method and obtain the output parameters.
set outParam = svc.Execmethod("__SystemSecurity=@", "GetSD")
wscript.echo outparam.ReturnValue
' Format the security descriptor array
' in the SD parameter into one string to display.
objSD  = Join(outparam.SD,",")
wscript.echo objSD
' Release the out parameters object.
set outParam = nothing
```



<span data-ttu-id="29be4-109">如需詳細資訊，請參閱 [**SWbemMethod. InParameters**](swbemmethod-inparameters.md)。</span><span class="sxs-lookup"><span data-stu-id="29be4-109">For more information, see [**SWbemMethod.InParameters**](swbemmethod-inparameters.md).</span></span>

 

 



