---
title: 設定實體和內容轉譯模式
description: 藉由設定實體和內容轉譯模式，WinSNMP 應用程式可以指定實體和內容參數的解讀和轉譯。 Microsoft WinSNMP 執行會將模式儲存在資料庫中。
ms.assetid: 2550f235-1351-440a-8b4e-f0d30b058229
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a50b5ecfb1a4703795f970f5d7c13ceaa3d64980
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021151"
---
# <a name="setting-the-entity-and-context-translation-mode"></a><span data-ttu-id="c2976-104">設定實體和內容轉譯模式</span><span class="sxs-lookup"><span data-stu-id="c2976-104">Setting the Entity and Context Translation Mode</span></span>

<span data-ttu-id="c2976-105">藉由設定實體和內容轉譯模式，WinSNMP 應用程式可以指定實體和內容參數的解讀和轉譯。</span><span class="sxs-lookup"><span data-stu-id="c2976-105">The WinSNMP application can specify the interpretation and translation of entity and context parameters by setting the entity and context translation mode.</span></span> <span data-ttu-id="c2976-106">Microsoft WinSNMP 執行會將模式儲存在資料庫中。</span><span class="sxs-lookup"><span data-stu-id="c2976-106">The Microsoft WinSNMP implementation stores the mode in a database.</span></span>

<span data-ttu-id="c2976-107">實體和內容轉譯模式的設定會決定 [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) 函式和 [**SnmpStrToCoNtext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) 函數解讀輸入字串的方式。</span><span class="sxs-lookup"><span data-stu-id="c2976-107">The setting of the entity and context translation mode determines the manner in which the [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) function and the [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) function interpret input strings.</span></span> <span data-ttu-id="c2976-108">這項設定也會決定 [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) 和 [**SnmpCoNtextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) 函數傳回的輸出字串類型。</span><span class="sxs-lookup"><span data-stu-id="c2976-108">The setting also determines the type of output string that the [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) and the [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) functions return.</span></span> <span data-ttu-id="c2976-109">如需詳細資訊，請參閱 [在 WinSNMP 中支援 IPX 位址字串](support-for-ipx-address-strings-in-winsnmp.md)。</span><span class="sxs-lookup"><span data-stu-id="c2976-109">For more information, see [Support for IPX Address Strings in WinSNMP](support-for-ipx-address-strings-in-winsnmp.md).</span></span>

<span data-ttu-id="c2976-110">在 [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup)函數的 *nTranslateMode* 參數中，此實值會傳回目前的預設實體和內容轉譯模式。</span><span class="sxs-lookup"><span data-stu-id="c2976-110">The implementation returns the current default entity and context translation mode in the *nTranslateMode* parameter of the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function.</span></span> <span data-ttu-id="c2976-111">若要取得目前的實體和實際執行的內容轉譯模式，應用程式可以在任何時間呼叫 [**SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode) 函數。</span><span class="sxs-lookup"><span data-stu-id="c2976-111">To retrieve the current entity and context translation mode in effect for the implementation, an application can call the [**SnmpGetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettranslatemode) function at any time.</span></span>

<span data-ttu-id="c2976-112">有效的實體和內容轉譯模式如下。</span><span class="sxs-lookup"><span data-stu-id="c2976-112">The valid entity and context translation modes follow.</span></span>

| <span data-ttu-id="c2976-113">模式</span><span class="sxs-lookup"><span data-stu-id="c2976-113">Mode</span></span>                      | <span data-ttu-id="c2976-114">意義</span><span class="sxs-lookup"><span data-stu-id="c2976-114">Meaning</span></span>                                                                                                                                                                                                                                                                                   |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2976-115">SNMPAPI \_ 轉譯</span><span class="sxs-lookup"><span data-stu-id="c2976-115">SNMPAPI\_TRANSLATED</span></span>       | <span data-ttu-id="c2976-116">此執行會使用其資料庫來轉譯 SNMP 實體和 managed 物件的使用者易記名稱。</span><span class="sxs-lookup"><span data-stu-id="c2976-116">The implementation uses its database to translate user-friendly names for SNMP entities and managed objects.</span></span> <span data-ttu-id="c2976-117">此執行會將它們轉譯成其 SNMPv1 或 SNMPv2C 元件。</span><span class="sxs-lookup"><span data-stu-id="c2976-117">The implementation translates them into their SNMPv1 or SNMPv2C components.</span></span>                                                                                                  |
| <span data-ttu-id="c2976-118">SNMPAPI 未 \_ 翻譯 \_ V1</span><span class="sxs-lookup"><span data-stu-id="c2976-118">SNMPAPI\_UNTRANSLATED\_V1</span></span> | <span data-ttu-id="c2976-119">此執行會將 SNMP 實體參數視為常值 snmp 傳輸位址，並將內容參數視為常值 SNMP 社區字串。</span><span class="sxs-lookup"><span data-stu-id="c2976-119">The implementation interprets SNMP entity parameters as literal SNMP transport addresses, and context parameters as literal SNMP community strings.</span></span> <span data-ttu-id="c2976-120">針對 SNMPv2 目的地實體，執行會在 [版本] 欄位中建立包含值為零的外寄 SNMP 訊息。</span><span class="sxs-lookup"><span data-stu-id="c2976-120">For SNMPv2 destination entities, the implementation creates outgoing SNMP messages that contain a value of zero in the version field.</span></span> |
| <span data-ttu-id="c2976-121">SNMPAPI 未 \_ 翻譯 \_ V2</span><span class="sxs-lookup"><span data-stu-id="c2976-121">SNMPAPI\_UNTRANSLATED\_V2</span></span> | <span data-ttu-id="c2976-122">此執行會將 SNMP 實體參數解讀為 SNMP 傳輸位址，並將內容參數視為常值 SNMP 的社區字串。</span><span class="sxs-lookup"><span data-stu-id="c2976-122">The implementation interprets SNMP entity parameters as SNMP transport addresses, and context parameters as literal SNMP community strings.</span></span> <span data-ttu-id="c2976-123">針對 SNMPv2 目的地實體，執行會在 [版本] 欄位中建立包含值1的外寄 SNMP 訊息。</span><span class="sxs-lookup"><span data-stu-id="c2976-123">For SNMPv2 destination entities, the implementation creates outgoing SNMP messages that contain a value of 1 in the version field.</span></span>            |



 

<span data-ttu-id="c2976-124">執行會嘗試將其資料庫中的資源與管理實體的常值傳輸位址產生關聯。</span><span class="sxs-lookup"><span data-stu-id="c2976-124">The implementation tries to associate resources in its database with the literal transport address of the management entity.</span></span>

<span data-ttu-id="c2976-125">若要變更實體和內容轉譯模式，設定 WinSNMP 應用程式必須呼叫 [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) 函數。</span><span class="sxs-lookup"><span data-stu-id="c2976-125">To change the entity and context translation mode setting a WinSNMP application must call the [**SnmpSetTranslateMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettranslatemode) function.</span></span> <span data-ttu-id="c2976-126">如果要求的轉譯模式無效，函數會失敗，而 [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) 會傳回錯誤碼 SNMPAPI \_ 模式 \_ 無效。</span><span class="sxs-lookup"><span data-stu-id="c2976-126">If the requested translation mode is invalid, the function fails, and [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) returns the error code SNMPAPI\_MODE\_INVALID.</span></span>

 

 




