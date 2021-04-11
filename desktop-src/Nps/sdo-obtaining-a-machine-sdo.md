---
title: 取得電腦 SDO
description: 使用 SDO API 的第一個步驟是建立 SDO 電腦物件。
ms.assetid: bdb01437-08d0-4279-94f2-840cb786cc44
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bf85f9712e76bbdadcffa3914a86cc56576aecd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023727"
---
# <a name="obtaining-a-machine-sdo"></a><span data-ttu-id="2b4cd-103">取得電腦 SDO</span><span class="sxs-lookup"><span data-stu-id="2b4cd-103">Obtaining a Machine SDO</span></span>

<span data-ttu-id="2b4cd-104">使用 SDO API 的第一個步驟是建立 SDO 電腦物件。</span><span class="sxs-lookup"><span data-stu-id="2b4cd-104">The first step in using the SDO API is to create an SDO machine object.</span></span>

<span data-ttu-id="2b4cd-105">您可以使用 [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) 函式來取得 SDO 電腦物件 (CLSID) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b4cd-105">Use the [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) function to obtain the class identifier (CLSID) for the SDO machine object.</span></span> <span data-ttu-id="2b4cd-106">用於物件 (ProgID) 的程式設計識別碼是「IAS」。SdoMachine".</span><span class="sxs-lookup"><span data-stu-id="2b4cd-106">The programmatic identifier (ProgID) to use for the object is "IAS.SdoMachine".</span></span>

<span data-ttu-id="2b4cd-107">有了 CLSID 之後，請使用此 CLSID 呼叫 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 。</span><span class="sxs-lookup"><span data-stu-id="2b4cd-107">Once you have the CLSID, call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with this CLSID.</span></span> <span data-ttu-id="2b4cd-108">將 [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) 指定為要傳回指標的介面。</span><span class="sxs-lookup"><span data-stu-id="2b4cd-108">Specify [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) as the interface for which to return a pointer.</span></span>

<span data-ttu-id="2b4cd-109">請參閱 [附加至 SDO-Enabled 電腦](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) ，取得示範如何取得電腦 SDO 的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="2b4cd-109">See [Attaching to an SDO-Enabled Computer](/windows/desktop/Nps/sdo-attaching-to-an-sdo-enabled-computer) for sample code that demonstrates how to obtain a machine SDO.</span></span>

 

 