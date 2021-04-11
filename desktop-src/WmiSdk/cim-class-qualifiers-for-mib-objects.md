---
description: 當將 MIB 物件定義對應至 CIM 類別定義時，SNMP 提供者會使用下列 CIM 類別限定詞。
ms.assetid: 458167dc-562e-47b8-8760-797ae13f9459
ms.tgt_platform: multiple
title: MIB 物件的 CIM 類別限定詞
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60fe97debc7fd81b48a6daf0f5a955374546458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194491"
---
# <a name="cim-class-qualifiers-for-mib-objects"></a><span data-ttu-id="b821a-103">MIB 物件的 CIM 類別限定詞</span><span class="sxs-lookup"><span data-stu-id="b821a-103">CIM Class Qualifiers for MIB Objects</span></span>

<span data-ttu-id="b821a-104">當將 MIB 物件定義對應至 CIM 類別定義時，SNMP 提供者會使用下列 CIM 類別限定詞。</span><span class="sxs-lookup"><span data-stu-id="b821a-104">The SNMP Provider uses the following CIM class qualifiers when mapping MIB object definitions to CIM class definitions.</span></span> <span data-ttu-id="b821a-105">SNMP 提供者必須要有必要的限定詞，才能完全解析群組物件。</span><span class="sxs-lookup"><span data-stu-id="b821a-105">A mandatory qualifier must be present for the SNMP Provider to fully resolve a group object.</span></span> <span data-ttu-id="b821a-106">無法定義強制辨識符號會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b821a-106">Failure to define a mandatory qualifier returns an error.</span></span> <span data-ttu-id="b821a-107">指定不合法的辨識符號值也會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="b821a-107">Specifying an illegal qualifier value also returns an error.</span></span>

> [!Note]  
> <span data-ttu-id="b821a-108">如需安裝提供者的詳細資訊，請參閱 [設定 WMI SNMP 環境](setting-up-the-wmi-snmp-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="b821a-108">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 



| <span data-ttu-id="b821a-109">Qualifier</span><span class="sxs-lookup"><span data-stu-id="b821a-109">Qualifier</span></span>           | <span data-ttu-id="b821a-110">描述</span><span class="sxs-lookup"><span data-stu-id="b821a-110">Description</span></span>                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b821a-111">**說明**</span><span class="sxs-lookup"><span data-stu-id="b821a-111">**Description**</span></span>     | <span data-ttu-id="b821a-112">**字串** 選</span><span class="sxs-lookup"><span data-stu-id="b821a-112">**string** Optional</span></span><br/> <span data-ttu-id="b821a-113">類別的描述。</span><span class="sxs-lookup"><span data-stu-id="b821a-113">Description of the class.</span></span><br/>                                                                      |
| <span data-ttu-id="b821a-114">**群組 \_ Objectid**</span><span class="sxs-lookup"><span data-stu-id="b821a-114">**Group\_Objectid**</span></span> | <span data-ttu-id="b821a-115">**字串** 如果是 SNMP 類別提供者的類別，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="b821a-115">**string** Mandatory, if the class is for the SNMP class provider.</span></span><br/> <span data-ttu-id="b821a-116">製造之集合的物件識別碼。</span><span class="sxs-lookup"><span data-stu-id="b821a-116">Object identifier of the fabricated collection.</span></span><br/> |
| <span data-ttu-id="b821a-117">**模組匯 \_ 入**</span><span class="sxs-lookup"><span data-stu-id="b821a-117">**Module\_Imports**</span></span> | <span data-ttu-id="b821a-118">**字串** 選</span><span class="sxs-lookup"><span data-stu-id="b821a-118">**string** Optional</span></span><br/> <span data-ttu-id="b821a-119">用來解析匯入之 MIB 模組名稱的逗號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="b821a-119">Comma-separated list of MIB module names used to resolve imports.</span></span><br/>                              |
| <span data-ttu-id="b821a-120">**模組 \_ 名稱**</span><span class="sxs-lookup"><span data-stu-id="b821a-120">**Module\_Name**</span></span>    | <span data-ttu-id="b821a-121">**字串** 選</span><span class="sxs-lookup"><span data-stu-id="b821a-121">**string** Optional</span></span><br/> <span data-ttu-id="b821a-122">MIB 模組的身分識別名稱。</span><span class="sxs-lookup"><span data-stu-id="b821a-122">Identity name of a MIB module.</span></span><br/>                                                                 |
| <span data-ttu-id="b821a-123">**參考**</span><span class="sxs-lookup"><span data-stu-id="b821a-123">**Reference**</span></span>       | <span data-ttu-id="b821a-124">**字串** 選</span><span class="sxs-lookup"><span data-stu-id="b821a-124">**string** Optional</span></span><br/> <span data-ttu-id="b821a-125">是指包含類別之詳細資訊的另一份檔。</span><span class="sxs-lookup"><span data-stu-id="b821a-125">Refers to another document that contains more information about the class.</span></span><br/>                     |
| <span data-ttu-id="b821a-126">**單身 人士**</span><span class="sxs-lookup"><span data-stu-id="b821a-126">**Singleton**</span></span>       | <span data-ttu-id="b821a-127">**Bool** 從純量集合對應之類別的必要參數。</span><span class="sxs-lookup"><span data-stu-id="b821a-127">**Bool** Mandatory for classes mapped from scalar collections.</span></span><br/> <span data-ttu-id="b821a-128">表示只能有一個實例的類別。</span><span class="sxs-lookup"><span data-stu-id="b821a-128">Indicates a class that can only have one instance.</span></span><br/>  |



 

 

 




