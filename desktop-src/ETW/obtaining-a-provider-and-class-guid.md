---
description: 若要取得提供者 GUID 或事件追蹤類別 Guid，您可以使用 Uuidgen.exe 或 Guidgen.exe 工具。
ms.assetid: 07483a78-ee67-4586-a75b-d376aa3351b7
title: 取得提供者和類別 GUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c12554cdb39459d824bf6622cd9d50e52f8c788d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973428"
---
# <a name="obtaining-a-provider-and-class-guid"></a><span data-ttu-id="01550-103">取得提供者和類別 GUID</span><span class="sxs-lookup"><span data-stu-id="01550-103">Obtaining a Provider and Class GUID</span></span>

<span data-ttu-id="01550-104">若要取得提供者 GUID 或事件追蹤類別 Guid，您可以使用 Uuidgen.exe 或 Guidgen.exe 工具。</span><span class="sxs-lookup"><span data-stu-id="01550-104">To obtain a provider GUID or event trace class GUIDs, you can use the Uuidgen.exe or Guidgen.exe tool.</span></span>

<span data-ttu-id="01550-105">如果您使用 Uuidgen.exe 工具，請使用-d 選項來建立定義 \_ GUID C 宏，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="01550-105">If you use the Uuidgen.exe tool, use the -d option to create a DEFINE\_GUID C macro, as shown in the following example.</span></span> <span data-ttu-id="01550-106">如需使用 Uuidgen.exe 工具的相關資訊，請使用-？</span><span class="sxs-lookup"><span data-stu-id="01550-106">For information about using the Uuidgen.exe tool, use the -?</span></span> <span data-ttu-id="01550-107">選項。</span><span class="sxs-lookup"><span data-stu-id="01550-107">option.</span></span> <span data-ttu-id="01550-108">如果您使用「定義 \_ Guid C」宏來定義您的 guid，您必須在 \# guid 定義之前包含「定義 INITGUID」，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="01550-108">If you use the DEFINE\_GUID C macro to define your GUID, you must include \#define INITGUID before your GUID definitions, as shown in the following example.</span></span>

``` syntax
#define INITGUID

DEFINE_GUID (
  ProviderGuid,
  0xf4dc272d, 
  0x88dd, 
  0x4472, 
  0xa3, 0xb1, 0xcb, 0x6d, 0xa4, 0x86, 0xf0, 0xbe
  );
```

<span data-ttu-id="01550-109">Microsoft Windows 軟體開發套件 (SDK) 和 Microsoft Visual Studio 包含 Guidgen.exe 工具。</span><span class="sxs-lookup"><span data-stu-id="01550-109">The Microsoft Windows Software Development Kit (SDK) and Microsoft Visual Studio include the Guidgen.exe tool.</span></span> <span data-ttu-id="01550-110">Guidgen.exe 工具有一個使用者介面，可讓您從數種格式中進行選取。</span><span class="sxs-lookup"><span data-stu-id="01550-110">The Guidgen.exe tool has a user interface that lets you select from several formats.</span></span> <span data-ttu-id="01550-111">您應使用可建立靜態常數 GUID 的格式，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="01550-111">You should use the format that creates a static constant GUID, as shown in the following example.</span></span>

``` syntax
// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };
```

 

 



