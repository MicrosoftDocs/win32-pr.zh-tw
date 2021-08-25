---
description: 網路監視器使用 ParserAutoInstallInfo export 函數來安裝剖析器。 呼叫 ParserAutoInstallInfo 時，剖析器會傳回一個 PF \_ PARSERDLLINFO 結構，其中包含安裝剖析器 DLL 時網路監視器所需的所有資訊。
ms.assetid: 1add9988-9cb2-43f9-8ae2-32acfe21b6f3
title: 執行 ParserAutoInstallInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6d1c797f53ad110392fea304cc0a610fdb0f9346c745e2f7dea2bff16208e05
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743078"
---
# <a name="implementing-parserautoinstallinfo"></a>執行 ParserAutoInstallInfo

網路監視器使用 [**ParserAutoInstallInfo**](parserautoinstallinfo.md) export 函數來安裝剖析器。 呼叫 **ParserAutoInstallInfo** 時，剖析器會傳回一個 [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md) 結構，其中包含安裝剖析器 DLL 時網路監視器所需的所有資訊。

> [!Note]  
> 網路監視器保留 [*Parser.ini*](p.md) 檔案中現有剖析器的清單，並為每個已安裝的剖析器建立個別的 INI 檔案。

 

在安裝過程中，剖析器 DLL 必須識別下列各項：

-   DLL 中的剖析器數目，包括每個剖析器的名稱和批註描述。
-   剖析器通訊協定前面的通訊協定。
-   遵循剖析器通訊協定的通訊協定。

> [!Note]  
> 網路監視器使用上述和後續的剖析器通訊協定資訊來更新 [*遞交集*](h.md) ，並遵循剖析器 DLL 識別的剖析器 [*集合*](f.md) 。

 

下列程式識別執行 [**ParserAutoInstallInfo**](parserautoinstallinfo.md)所需的步驟。

**若要執行 ParserAutoInstallInfo**

1.  使用 **HeapAlloc** 配置 [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md)結構。
2.  使用 **HeapFree** 將記憶體傳回至堆積。
3.  請注意，此呼叫也必須為 DLL 中的每個剖析器配置 [**PF \_ PARSERINFO**](pf-parserinfo.md) 結構。
4.  指定剖析器的數目 (通常是 DLL 在 [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md)的 **nParsers** 成員中包含的一個) 。
5.  在每個 [**PF \_ PARSERINFO**](pf-parserinfo.md)結構的 **SzProtocolName**、 **szComment** 和 **szHelpFile** 成員中，指定名稱、批註和選擇性的說明檔。
6.  指定每個 DLL 通訊協定前面的通訊協定。 下列其中一個條件適用于傳入的交付集。
    -   如果先前的通訊協定可以從先前的通訊協定中的資料來判斷您的通訊協定，請設定 [**PF \_ PARSERINFO**](pf-parserinfo.md)的 **pWhoHandsOffToMe** 成員。 在此情況下，系統會將您的通訊協定新增至上述通訊協定的 [*交付集*](h.md) 。
    -   如果先前的通訊協定無法從先前的通訊協定中的資料決定您的通訊協定，請設定 [**PF \_ PARSERINFO**](pf-parserinfo.md)的 **pWhoCanPrecedeMe** 成員。 在此情況下，您的通訊協定會新增至 [*下列*](f.md) 通訊協定組。
7.  指定遵循每個 DLL 通訊協定的通訊協定。 下列其中一項條件適用于傳出的後續設定。
    -   如果您的通訊協定可以根據通訊協定中的資料來判斷要遵循的通訊協定，請設定 [**PF \_ PARSERINFO**](pf-parserinfo.md)的 **pWhoDoIHandOffTo** 成員。 在此情況下，這些通訊協定會新增到您的通訊協定的 [*一組遞交*](h.md) 中。
    -   如果您的通訊協定無法根據通訊協定中的資料來判斷要遵循的通訊協定，請設定 [**PF \_ PARSERINFO**](pf-parserinfo.md)的 **pWhoCanFollowMe** 成員。 在此情況下，這些通訊協定會新增至通訊協定的 [*下列集合*](f.md) 。
8.  將 [**PF \_ PARSERDLLINFO**](pf-parserdllinfo.md) 結構傳回網路監視器。

以下是 [**ParserAutoInstallInfo**](parserautoinstallinfo.md)的基本執行。 程式碼範例取自網路監視器提供的泛型剖析器。

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

 

 



