---
description: 網路監視器從 capture 檔案載入 capture，然後開始針對它可以識別的所有通訊協定，呼叫 Register 函數。 每個剖析器 DLL 都必須針對剖析器 DLL 支援的每個通訊協定來執行 Register 函數。
ms.assetid: a53c64cb-569f-454b-ae85-7b850228c954
title: 執行註冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b59f34f5f97925627184db7188aac0a9eb796a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975923"
---
# <a name="implementing-register"></a><span data-ttu-id="4d2d0-104">執行註冊</span><span class="sxs-lookup"><span data-stu-id="4d2d0-104">Implementing Register</span></span>

<span data-ttu-id="4d2d0-105">網路監視器從 capture 檔案載入 capture，然後開始針對它可以識別的所有通訊協定，呼叫 [**Register**](register-parser.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-105">Network Monitor loads a capture from the capture file, and then starts calling the [**Register**](register-parser.md) function for all the protocols that it can identify.</span></span> <span data-ttu-id="4d2d0-106">每個剖析器 DLL 都必須針對剖析器 DLL 支援的每個通訊協定來執行 **Register** 函數。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-106">Each parser DLL must implement a **Register** function for each protocol that the parser DLL supports.</span></span>

<span data-ttu-id="4d2d0-107">[**註冊**](register-parser.md)函式的每個實作為都必須呼叫 [**CreatePropertyDatabase**](createpropertydatabase.md)和 [**AddProperty**](/previous-versions/bb251873(v=msdn.10))函式，以建立並填入通訊協定的 [*屬性資料庫*](p.md)，然後建立 [**CreateHandoffTable**](createhandofftable.md)來建立通訊協定的 [*遞交資料表*](h.md)（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-107">Each implementation of the [**Register**](register-parser.md) function must call the [**CreatePropertyDatabase**](createpropertydatabase.md) and [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) functions to create and fill-in the [*property database*](p.md) for the protocol, and then the [**CreateHandoffTable**](createhandofftable.md) to create the [*handoff table*](h.md) for the protocol — if needed.</span></span>

> [!Note]  
> <span data-ttu-id="4d2d0-108">針對網路監視器定義了通訊協定屬性。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-108">Protocol properties are defined for Network Monitor.</span></span> <span data-ttu-id="4d2d0-109">在呼叫 [**AttachProperties**](attachproperties.md) 匯出函式之前，屬性不會對應至 capture 資料中的位置。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-109">Properties are not mapped to a location in a capture data until the [**AttachProperties**](attachproperties.md) export function is called.</span></span>

 

<span data-ttu-id="4d2d0-110">下列程式識別執行 [**Register**](register-parser.md) 函數所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-110">The following procedure identifies the steps necessary to implement the [**Register**](register-parser.md) function.</span></span>

<span data-ttu-id="4d2d0-111">**若要執行一個通訊協定的註冊**</span><span class="sxs-lookup"><span data-stu-id="4d2d0-111">**To implement Register for one protocol**</span></span>

1.  <span data-ttu-id="4d2d0-112">定義 [**PROPERTYINFO**](propertyinfo.md) 結構的陣列，以描述該通訊協定支援的每個屬性。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-112">Define an array of [**PROPERTYINFO**](propertyinfo.md) structures to describe each property that the protocol supports.</span></span>
2.  <span data-ttu-id="4d2d0-113">呼叫 [**CreatePropertyDatabase**](createpropertydatabase.md) 來提供通訊協定控制碼，以及通訊協定支援的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-113">Call [**CreatePropertyDatabase**](createpropertydatabase.md) to provide a protocol handle, and the number of properties that the protocol supports.</span></span>
3.  <span data-ttu-id="4d2d0-114">在迴圈中呼叫 [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) ，以加入 [**PROPERTYINFO**](propertyinfo.md) 結構陣列中定義的每個屬性。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-114">Call [**AddProperty**](/previous-versions/bb251873(v=msdn.10)) in a loop to add each property defined in the [**PROPERTYINFO**](propertyinfo.md) structure array.</span></span>
4.  <span data-ttu-id="4d2d0-115">如果通訊協定使用「提交」資料表，請在所有的通訊協定屬性都加入至屬性資料庫之後，呼叫 [**CreateHandoffTable**](createhandofftable.md)。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-115">If the protocol uses a handoff table, call [**CreateHandoffTable**](createhandofftable.md)— after all the properties of the protocol are added to the property database.</span></span>

<span data-ttu-id="4d2d0-116">以下是 [**Register**](register-parser.md)的基本執行。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-116">The following is a basic implementation of [**Register**](register-parser.md).</span></span> <span data-ttu-id="4d2d0-117">請注意，屬性資料庫是針對僅支援兩個屬性的通訊協定所建立。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-117">Note that a property database is created for a protocol that supports only two properties.</span></span> <span data-ttu-id="4d2d0-118">這個程式碼範例取自網路監視器提供的泛型剖析器。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-118">This code example is taken from the generic parser that Network Monitor provides.</span></span>

``` syntax
#include <windows.h>

PROPERTYINFO MyProtocolPropertyTable[]
{
  // Summary property (0)
  {
     0,                               // Handle to property.
     0,                               // Reserved.
     "Summary",                       // Property label.
     "Summary of protocol packet",    // Property comment.
     PROP_TYPE_SUMMARY,               // Data type of property.
     PROP_QUAL_NONE,                  // Data type qualifier.
     NULL,                            // Reserved.
     80,                              // 
     FormatPropertyInstance           // 
  }

  // WORD property (1)
  {
     0,                               // Handle to property.
     0,                               // Reserved.
     "WORD property",                 // Property label.
     "16-bit WORD property",         // Property comment.
     PROP_TYPE_WORD,                  // Data type of property.
     PROP_QUAL_NONE,                  // Data type qualifier.
     NULL,                            // Reserved.
     80,                              // 
     FormatPropertyInstance           // 
  }

}

void BHAPI MyProtocolRegister( HPPROTOCOL hProtocol) 
{
  // Create property database.
  DWORD dwNumberOfProperties = 2;
  CreatePropertyDatabase (hProtocol,
                          dwNumberOfProperties
                          );
  
  // Add properties to database.
  WORD i;
  for( i=0; i< dwNumberOfProperties; i++)
  {
     AddProperty(hProtocol, &MyProtocolPropertyTable[i]);
  }

  // Create handoff table.
  CreateHandoffTable("myProtocolHandoffTable",
                          "myProtocol.ini",
                           hTable,
                           MaxEntries,
                           10       // Handoff set values are base 10.
                          )
}
```

 

 
