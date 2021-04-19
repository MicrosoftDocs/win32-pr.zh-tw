---
description: SNMP 集合會對應到 CIM 類別，而集合的元素會對應至 CIM 類別的屬性。 所有產生的 CIM 類別定義都必須衍生自 SnmpObjectType 類別。
ms.assetid: e6f82fd6-e3d8-48c5-8c7b-a30a2d502f41
ms.tgt_platform: multiple
title: SNMP 集合
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a85473a394ce715ff9759e974a47824e5621509f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974192"
---
# <a name="snmp-collections"></a><span data-ttu-id="1d664-104">SNMP 集合</span><span class="sxs-lookup"><span data-stu-id="1d664-104">SNMP Collections</span></span>

<span data-ttu-id="1d664-105">SNMP 集合會對應到 CIM 類別，而集合的元素會對應至 CIM 類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="1d664-105">An SNMP collection maps to a CIM class and the elements of a collection map to the properties of a CIM class.</span></span> <span data-ttu-id="1d664-106">所有產生的 CIM 類別定義都必須衍生自 **SnmpObjectType** 類別。</span><span class="sxs-lookup"><span data-stu-id="1d664-106">All generated CIM class definitions must be derived from the **SnmpObjectType** class.</span></span>

> [!Note]  
> <span data-ttu-id="1d664-107">如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="1d664-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="1d664-108">下列類別定義父代所有產生的類別定義：</span><span class="sxs-lookup"><span data-stu-id="1d664-108">The following class definitions parent all generated class definitions:</span></span>

``` syntax
[abstract]
class SnmpMacro
{
};

[abstract]
class SnmpObjectType:SnmpMacro
{
};
```

## <a name="remarks"></a><span data-ttu-id="1d664-109">備註</span><span class="sxs-lookup"><span data-stu-id="1d664-109">Remarks</span></span>

<span data-ttu-id="1d664-110">將 SNMP 集合對應至 CIM 類別時，適用下列規則。</span><span class="sxs-lookup"><span data-stu-id="1d664-110">The following rules apply when mapping SNMP collections to CIM classes.</span></span> <span data-ttu-id="1d664-111">除非另有指定，否則這些規則適用于純量和資料表集合：</span><span class="sxs-lookup"><span data-stu-id="1d664-111">Unless otherwise specified, these rules apply to both scalar and table collections:</span></span>

-   <span data-ttu-id="1d664-112">對應程式會串連 "SNMP \_ "、MIB 模組識別名稱、" \_ " 和集合的物件描述元，以產生 CIM 類別名稱。</span><span class="sxs-lookup"><span data-stu-id="1d664-112">The mapping process generates CIM class names by concatenating "SNMP\_", the MIB module identity name, "\_", and the collection's object descriptor.</span></span>

    <span data-ttu-id="1d664-113">例如： **系統** 會轉譯為 **snmp \_ RFC1213 \_ MIB \_ 系統**，而 **ifTable** 則會轉譯為 **snmp \_ RFC1213 \_ mib \_ ifTable**。</span><span class="sxs-lookup"><span data-stu-id="1d664-113">For example: **system** translates to **SNMP\_RFC1213\_MIB\_system**, while **ifTable** translates to **SNMP\_RFC1213\_MIB\_ifTable**.</span></span>

-   <span data-ttu-id="1d664-114">在所有情況下，SNMP MIB 識別碼中的連字號 ( ) 會對應到 \_ CIM 類別名稱中的底線 () 。</span><span class="sxs-lookup"><span data-stu-id="1d664-114">In all cases, hyphens (-) in SNMP MIB identifiers map to underscores (\_) in CIM class names.</span></span>
-   <span data-ttu-id="1d664-115">由於 CIM 名稱不區分大小寫，因此可能會發生命名衝突。</span><span class="sxs-lookup"><span data-stu-id="1d664-115">Naming conflicts can occur due to CIM name case-insensitivity.</span></span> <span data-ttu-id="1d664-116">如果發生命名衝突，提供者會選擇其中一個衝突的群組定義，並忽略其餘的定義。</span><span class="sxs-lookup"><span data-stu-id="1d664-116">If a naming conflict occurs, the provider chooses one of the conflicting group definitions and ignores the remaining definitions.</span></span>
-   <span data-ttu-id="1d664-117">包含集合的 MIB 模組的身分識別名稱會對應到 CIM 類別限定詞 **模組 \_ 名稱**。</span><span class="sxs-lookup"><span data-stu-id="1d664-117">The identity name of the MIB module that contains the collection maps to the CIM class qualifier **Module\_Name**.</span></span>
-   <span data-ttu-id="1d664-118">製造集合的物件識別碼會對應至 CIM 類別限定詞 **群組 \_ Objectid**。</span><span class="sxs-lookup"><span data-stu-id="1d664-118">The object identifier of the fabricated collection maps to the CIM class qualifier **Group\_Objectid**.</span></span>
-   <span data-ttu-id="1d664-119">從 **模組身分識別** 巨集定義取得的 MIB 模組匯入清單 (，) 對應至 CIM 類別限定詞 **模組匯 \_ 入**。</span><span class="sxs-lookup"><span data-stu-id="1d664-119">The MIB module imports list (obtained from the **MODULE-IDENTITY** macro definition) maps to the CIM class qualifier **module\_imports**.</span></span> <span data-ttu-id="1d664-120">此限定詞包含以逗號分隔的模組名稱清單。</span><span class="sxs-lookup"><span data-stu-id="1d664-120">This qualifier contains a comma-separated list of module names.</span></span>

 

 



