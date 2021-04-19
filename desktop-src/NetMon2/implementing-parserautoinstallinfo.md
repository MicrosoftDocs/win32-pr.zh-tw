---
description: 網路監視器使用 ParserAutoInstallInfo export 函數來安裝剖析器。 呼叫 ParserAutoInstallInfo 時，剖析器會傳回一個 PF \_ PARSERDLLINFO 結構，其中包含安裝剖析器 DLL 時網路監視器所需的所有資訊。
ms.assetid: 1add9988-9cb2-43f9-8ae2-32acfe21b6f3
title: 執行 ParserAutoInstallInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d79a9ba5036673acb076be9f3634dae7556b5bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979996"
---
# <a name="implementing-parserautoinstallinfo"></a><span data-ttu-id="62591-104">執行 ParserAutoInstallInfo</span><span class="sxs-lookup"><span data-stu-id="62591-104">Implementing ParserAutoInstallInfo</span></span>

<span data-ttu-id="62591-105">網路監視器使用 [**ParserAutoInstallInfo**](parserautoinstallinfo.md) export 函數來安裝剖析器。</span><span class="sxs-lookup"><span data-stu-id="62591-105">Network Monitor uses the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) export function to install a parser.</span></span> <span data-ttu-id="62591-106">呼叫 **ParserAutoInstallInfo** 時，剖析器會傳回一個 [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md) 結構，其中包含安裝剖析器 DLL 時網路監視器所需的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="62591-106">When **ParserAutoInstallInfo** is called, the parser returns a [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure containing all the information that Network Monitor needs to install a parser DLL.</span></span>

> [!Note]  
> <span data-ttu-id="62591-107">網路監視器保留 [*Parser.ini*](p.md) 檔案中現有剖析器的清單，並為每個已安裝的剖析器建立個別的 INI 檔案。</span><span class="sxs-lookup"><span data-stu-id="62591-107">Network Monitor keeps a list of existing parsers in the [*Parser.ini*](p.md) file, and creates a separate INI file for each installed parser.</span></span>

 

<span data-ttu-id="62591-108">在安裝過程中，剖析器 DLL 必須識別下列各項：</span><span class="sxs-lookup"><span data-stu-id="62591-108">During the installation process, the parser DLL must identify the following:</span></span>

-   <span data-ttu-id="62591-109">DLL 中的剖析器數目，包括每個剖析器的名稱和批註描述。</span><span class="sxs-lookup"><span data-stu-id="62591-109">The number of parsers in the DLL—including a name and comment description for each parser.</span></span>
-   <span data-ttu-id="62591-110">剖析器通訊協定前面的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="62591-110">The protocols that precede the parser protocol.</span></span>
-   <span data-ttu-id="62591-111">遵循剖析器通訊協定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="62591-111">The protocols that follow the parser protocol.</span></span>

> [!Note]  
> <span data-ttu-id="62591-112">網路監視器使用上述和後續的剖析器通訊協定資訊來更新 [*遞交集*](h.md) ，並遵循剖析器 DLL 識別的剖析器 [*集合*](f.md) 。</span><span class="sxs-lookup"><span data-stu-id="62591-112">Network Monitor uses the preceding and following parser protocol information to update the [*handoff sets*](h.md) and [*follow sets*](f.md) of parsers that your parser DLL identifies.</span></span>

 

<span data-ttu-id="62591-113">下列程式識別執行 [**ParserAutoInstallInfo**](parserautoinstallinfo.md)所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="62591-113">The following procedure identifies the steps necessary to implement [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span></span>

<span data-ttu-id="62591-114">**若要執行 ParserAutoInstallInfo**</span><span class="sxs-lookup"><span data-stu-id="62591-114">**To implement ParserAutoInstallInfo**</span></span>

1.  <span data-ttu-id="62591-115">使用 **HeapAlloc** 配置 [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md)結構。</span><span class="sxs-lookup"><span data-stu-id="62591-115">Allocate a [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure using **HeapAlloc**.</span></span>
2.  <span data-ttu-id="62591-116">使用 **HeapFree** 將記憶體傳回至堆積。</span><span class="sxs-lookup"><span data-stu-id="62591-116">Return memory to the heap using **HeapFree**.</span></span>
3.  <span data-ttu-id="62591-117">請注意，此呼叫也必須為 DLL 中的每個剖析器配置 [**PF \_ PARSERINFO**](pf-parserinfo.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="62591-117">Be aware that this call must also allocate a [**PF\_PARSERINFO**](pf-parserinfo.md) structure for each parser in the DLL.</span></span>
4.  <span data-ttu-id="62591-118">指定剖析器的數目 (通常是 DLL 在 [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md)的 **nParsers** 成員中包含的一個) 。</span><span class="sxs-lookup"><span data-stu-id="62591-118">Specify the number of parsers (typically one) that the DLL contains in the **nParsers** member of [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md).</span></span>
5.  <span data-ttu-id="62591-119">在每個 [**PF \_ PARSERINFO**](pf-parserinfo.md)結構的 **SzProtocolName**、 **szComment** 和 **szHelpFile** 成員中，指定名稱、批註和選擇性的說明檔。</span><span class="sxs-lookup"><span data-stu-id="62591-119">Specify a name, comment, and optional Help file in the **szProtocolName**, **szComment**, and **szHelpFile** members of each [**PF\_PARSERINFO**](pf-parserinfo.md) structure.</span></span>
6.  <span data-ttu-id="62591-120">指定每個 DLL 通訊協定前面的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="62591-120">Specify the protocols that precede each DLL protocol.</span></span> <span data-ttu-id="62591-121">下列其中一個條件適用于傳入的交付集。</span><span class="sxs-lookup"><span data-stu-id="62591-121">One of the following conditions applies to an incoming handoff set.</span></span>
    -   <span data-ttu-id="62591-122">如果先前的通訊協定可以從先前的通訊協定中的資料來判斷您的通訊協定，請設定 [**PF \_ PARSERINFO**](pf-parserinfo.md)的 **pWhoHandsOffToMe** 成員。</span><span class="sxs-lookup"><span data-stu-id="62591-122">If the preceding protocols can determine that your protocol follows from data in the preceding protocols, set the **pWhoHandsOffToMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="62591-123">在此情況下，系統會將您的通訊協定新增至上述通訊協定的 [*交付集*](h.md) 。</span><span class="sxs-lookup"><span data-stu-id="62591-123">In this case, your protocol is then added to the [*handoff sets*](h.md) of the preceding protocols.</span></span>
    -   <span data-ttu-id="62591-124">如果先前的通訊協定無法從先前的通訊協定中的資料決定您的通訊協定，請設定 [**PF \_ PARSERINFO**](pf-parserinfo.md)的 **pWhoCanPrecedeMe** 成員。</span><span class="sxs-lookup"><span data-stu-id="62591-124">If the preceding protocols cannot determine that your protocol follows from data in the preceding protocols, set **pWhoCanPrecedeMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="62591-125">在此情況下，您的通訊協定會新增至 [*下列*](f.md) 通訊協定組。</span><span class="sxs-lookup"><span data-stu-id="62591-125">In this case, the your protocol is then added to the [*follow sets*](f.md) of the protocols.</span></span>
7.  <span data-ttu-id="62591-126">指定遵循每個 DLL 通訊協定的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="62591-126">Specify the protocols that follow each DLL protocol.</span></span> <span data-ttu-id="62591-127">下列其中一項條件適用于傳出的後續設定。</span><span class="sxs-lookup"><span data-stu-id="62591-127">One of the following conditions applies to an outgoing follow-set.</span></span>
    -   <span data-ttu-id="62591-128">如果您的通訊協定可以根據通訊協定中的資料來判斷要遵循的通訊協定，請設定 [**PF \_ PARSERINFO**](pf-parserinfo.md)的 **pWhoDoIHandOffTo** 成員。</span><span class="sxs-lookup"><span data-stu-id="62591-128">If your protocol can determine which protocols follow based on data in your protocol, set the **pWhoDoIHandOffTo** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="62591-129">在此情況下，這些通訊協定會新增到您的通訊協定的 [*一組遞交*](h.md) 中。</span><span class="sxs-lookup"><span data-stu-id="62591-129">In this case, the these protocols are added to the [*handoff set*](h.md) of your protocols.</span></span>
    -   <span data-ttu-id="62591-130">如果您的通訊協定無法根據通訊協定中的資料來判斷要遵循的通訊協定，請設定 [**PF \_ PARSERINFO**](pf-parserinfo.md)的 **pWhoCanFollowMe** 成員。</span><span class="sxs-lookup"><span data-stu-id="62591-130">If your protocol cannot determine which protocols follow based on data in your protocol, set the **pWhoCanFollowMe** member of [**PF\_PARSERINFO**](pf-parserinfo.md).</span></span> <span data-ttu-id="62591-131">在此情況下，這些通訊協定會新增至通訊協定的 [*下列集合*](f.md) 。</span><span class="sxs-lookup"><span data-stu-id="62591-131">In this case, these protocols are added to the [*follow set*](f.md) of your protocol.</span></span>
8.  <span data-ttu-id="62591-132">將 [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md) 結構傳回網路監視器。</span><span class="sxs-lookup"><span data-stu-id="62591-132">Return the [**PF\_PARSERDLLINFO**](pf-parserdllinfo.md) structure to Network Monitor.</span></span>

<span data-ttu-id="62591-133">以下是 [**ParserAutoInstallInfo**](parserautoinstallinfo.md)的基本執行。</span><span class="sxs-lookup"><span data-stu-id="62591-133">The following is a basic implementation of [**ParserAutoInstallInfo**](parserautoinstallinfo.md).</span></span> <span data-ttu-id="62591-134">程式碼範例取自網路監視器提供的泛型剖析器。</span><span class="sxs-lookup"><span data-stu-id="62591-134">The code example is taken from the generic parser that Network Monitor provides.</span></span>

``` syntax
#include <windows.h>

PPF_PARSERDLLINFO WINAPI ParserAutoInstallInfo() 
{

  /////////////////////////////////////////////////////////////////
  //
  // Allocate memory for PF_PARSERDLLINFO structure.
  //
  /////////////////////////////////////////////////////////////////
  PPF_PARSERDLLINFO pParserDllInfo; 
  PPF_PARSERINFO    pParserInfo;
  DWORD NumProtocols;
        DWORD NumParsers;
        DWORD NumFollows;
  NumParsers = 1;
  
  pParserDllInfo = (PPF_PARSERDLLINFO)HeapAlloc( GetProcessHeap(),
                                                 HEAP_ZERO_MEMORY,
                                                 sizeof( PF_PARSERDLLINFO ) +
                                                 NumParsers * sizeof( PF_PARSERINFO) );
  if( pParserDllInfo == NULL)
  {
    return NULL;
  }
  

    
  /////////////////////////////////////////////////////////////////
  //
  // Specify the number of parsers in the DLL.
  //
  /////////////////////////////////////////////////////////////////
  
  pParserDllInfo->nParsers = NumParsers;
  

  /////////////////////////////////////////////////////////////////
  // 
  // Specify the name, comment, and Help file for each protocol.
  // 
  /////////////////////////////////////////////////////////////////
  pParserInfo = &(pParserDllInfo->ParserInfo[0]);
  sprintf_s( pParserInfo->szProtocolName, MAX_PROTOCOL_NAME_LEN, 
    "TestProtocol" );
  sprintf_s( pParserInfo->szComment, MAX_PROTOCOL_COMMENT_LEN,
    "Test protocol for SDK" );
  sprintf_s( pParserInfo->szHelpFile, MAX_PATH, "");
  

  
  /////////////////////////////////////////////////////////////////
  //
  // Specify preceding protocols.
  //
  /////////////////////////////////////////////////////////////////
  PPF_HANDOFFSET    pHandoffSet;
  PPF_HANDOFFENTRY  pHandoffEntry;
  
  // Allocate PF_HANDOFFSET structure.
  NumHandoffs = 1;                   
  pHandoffSet = (PPF_HANDOFFSET)HeapAlloc( GetProcessHeap(),
                                           HEAP_ZERO_MEMORY,
                                           sizeof( PF_HANDOFFSET ) +
                                           NumHandoffs * sizeof( PF_HANDOFFENTRY) );
  if( pHandoffSet == NULL )
  {
     return pParserDllInfo;
  }

  // Fill in handoff set
  pParserInfo->pWhoHandsOffToMe = pHandoffSet;
  pHandoffSet->nEntries = NumHandoffs;

  // TCP PORT FFFF
  pHandoffEntry = &(pHandoffSet->Entry[0]);
  sprintf_s( pHandoffEntry->szIniFile, MAX_PATH, "TCPIP.INI" );
  sprintf_s( pHandoffEntry->szIniSection, MAX_PATH, "TCP_HandoffSet" );
  sprintf_s( pHandoffEntry->szProtocol, MAX_PROTOCOL_NAME_LEN, 
    "BLRPLATE" );
  pHandoffEntry->dwHandOffValue =        0xFFFF;
  pHandoffEntry->ValueFormatBase =       HANDOFF_VALUE_FORMAT_BASE_DECIMAL;    
  
  

  /////////////////////////////////////////////////////////////////
  //
  // Specify the following protocols.
  //
  /////////////////////////////////////////////////////////////////
  PPF_FOLLOWSET     pFollowSet;
  PPF_FOLLOWENTRY   pFollowEntry;
 
  // Allocate PF_FOLLOWSET structure
  NumFollows = 1;
  pFollowSet = (PPF_FOLLOWSET)HeapAlloc( GetProcessHeap(),
                                         HEAP_ZERO_MEMORY,
                                         sizeof( PF_FOLLOWSET ) +
                                         NumFollows * sizeof( PF_FOLLOWENTRY) );
  if( pFollowSet == NULL )
  {
    return pParserDllInfo;
  }

  // Fill in the follow set
  pParserInfo->pWhoCanFollowMe = pFollowSet;
  pFollowSet->nEntries = NumFollows;

  // Add SMB
  pFollowEntry = &(pFollowSet->Entry[0]);
  sprintf_s( pFollowEntry->szProtocol, MAX_PROTOCOL_NAME_LEN, "SMB" );
  


  /////////////////////////////////////////////////////////////////
  //
  // Return the PF_PARSERDLLINFO structure.
  //
  /////////////////////////////////////////////////////////////////
  return pParserDllInfo;

}
```

 

 



