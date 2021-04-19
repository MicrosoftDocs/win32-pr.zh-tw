---
title: '>strsafe.h 函式'
description: .
ms.assetid: 3590dd8d-3a88-4dde-a5fe-f10e12354919
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b31824788b68a7ec789c6d274b2a368eda1cfc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "107001078"
---
# <a name="strsafe-functions"></a>>strsafe.h 函式

## <a name="in-this-section"></a>本節內容

-   [**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)
-   [**StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)
-   [**StringCbCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)
-   [**StringCbCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)
-   [**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)
-   [**StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)
-   [**StringCbCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)
-   [**StringCbCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)
-   [**StringCbGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)
-   [**StringCbGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)
-   [**StringCbLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)
-   [**StringCbPrintf \_ l**](/windows/desktop/api/StrSafe/nf-strsafe-stringcbprintf_la)
-   [**StringCbPrintf \_ lEx**](/windows/desktop/api/StrSafe/nf-strsafe-stringcbprintf_lexa)
-   [**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)
-   [**StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)
-   [**StringCbVPrintf \_ l**](/windows/desktop/api/StrSafe/nf-strsafe-stringcbvprintf_la)
-   [**StringCbVPrintf \_ lEx**](/windows/desktop/api/StrSafe/nf-strsafe-stringcbvprintf_lexa)
-   [**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)
-   [**StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)
-   [**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)
-   [**StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)
-   [**StringCchCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)
-   [**StringCchCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)
-   [**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)
-   [**StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)
-   [**StringCchCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)
-   [**StringCchCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)
-   [**StringCchGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)
-   [**StringCchGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)
-   [**StringCchLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)
-   [**StringCchPrintf \_ l**](/windows/desktop/api/StrSafe/nf-strsafe-stringcchprintf_la)
-   [**StringCchPrintf \_ lEx**](/windows/desktop/api/StrSafe/nf-strsafe-stringcchprintf_lexa)
-   [**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)
-   [**StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)
-   [**StringCchVPrintf \_ l**](/windows/desktop/api/StrSafe/nf-strsafe-stringcchvprintf_la)
-   [**StringCchVPrintf \_ lEx**](/windows/desktop/api/StrSafe/nf-strsafe-stringcchvprintf_lexa)
-   [**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)
-   [**StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)
-   [**UnalignedStringCbLength**](/previous-versions/windows/desktop/legacy/hh305643(v=vs.85))
-   [**UnalignedStringCchLength**](/previous-versions/windows/desktop/legacy/hh305644(v=vs.85))

 

 