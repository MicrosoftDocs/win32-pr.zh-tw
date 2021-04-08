---
title: C 樣式字串
description: WinSNMP 應用程式可以使用以 Null 結束的 C 樣式字串，將實體和物件識別碼 (OID) 物件轉換成其字串表示。
ms.assetid: df04071c-df46-410b-ad92-6adecbfcd454
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878398b6d8691982aa90b9f1376a38214030e52e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839099"
---
# <a name="c-style-strings"></a><span data-ttu-id="312dc-103">C 樣式字串</span><span class="sxs-lookup"><span data-stu-id="312dc-103">C-Style Strings</span></span>

<span data-ttu-id="312dc-104">WinSNMP 應用程式可以使用以 **Null** 結束的 C 樣式字串，將實體和物件識別碼 (OID) 物件轉換成其字串表示。</span><span class="sxs-lookup"><span data-stu-id="312dc-104">A WinSNMP application can use **NULL**-terminated C-style strings to convert entity and object identifier (OID) objects to and from their string representations.</span></span>

<span data-ttu-id="312dc-105">操作 C 樣式字串的 WinSNMP 函數包括 [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity)、 [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr)、 [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)和 [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr)。</span><span class="sxs-lookup"><span data-stu-id="312dc-105">The WinSNMP functions that manipulate C-style strings include [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid), and [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr).</span></span> <span data-ttu-id="312dc-106">因為 [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) 和 [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) 會傳回 C 樣式字串變數的指標，所以在呼叫這些函式時，WinSNMP 應用程式必須在 *size* 參數中傳遞適當的值。</span><span class="sxs-lookup"><span data-stu-id="312dc-106">Because [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) and [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) return a pointer to a C-style string variable, the WinSNMP application must pass an appropriate value in the *size* parameter when it makes calls to these functions.</span></span> <span data-ttu-id="312dc-107">如需詳細資訊，請參閱這些函數的參考頁面。</span><span class="sxs-lookup"><span data-stu-id="312dc-107">For more information, see the reference pages for these functions.</span></span>

> [!Note]  
> <span data-ttu-id="312dc-108">[**SnmpStrToCoNtext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext)和 [**SnmpCoNtextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr)函數的 *coNtext* 參數必須是八位字串結構，也就是 [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets)結構。</span><span class="sxs-lookup"><span data-stu-id="312dc-108">The *context* parameter of the [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) and [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) functions must be an octet string structure, that is, an [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) structure.</span></span> <span data-ttu-id="312dc-109">*內容* 參數不能是 C 樣式字串。</span><span class="sxs-lookup"><span data-stu-id="312dc-109">The *context* parameter cannot be a C-style string.</span></span> <span data-ttu-id="312dc-110">包含在 **smiOCTETS** 結構中的字串不需要 **Null** 終止位元組。</span><span class="sxs-lookup"><span data-stu-id="312dc-110">The string contained in an **smiOCTETS** structure does not require a **NULL**-terminating byte.</span></span>

 

 

 




