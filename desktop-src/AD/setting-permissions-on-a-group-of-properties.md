---
title: 設定屬性群組的許可權
description: 許可權可以套用至屬性的群組。
ms.assetid: cb9f6c04-be94-45b4-ba84-2a79b7625fdd
ms.tgt_platform: multiple
keywords:
- 設定 AD 屬性群組的許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3f2993a537b76b64c7e8e6323c850494b3ce306
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681635"
---
# <a name="setting-permissions-on-a-group-of-properties"></a><span data-ttu-id="d478e-104">設定屬性群組的許可權</span><span class="sxs-lookup"><span data-stu-id="d478e-104">Setting Permissions on a Group of Properties</span></span>

<span data-ttu-id="d478e-105">許可權可以套用至屬性的群組。</span><span class="sxs-lookup"><span data-stu-id="d478e-105">Permissions can be applied to a group of properties.</span></span> <span data-ttu-id="d478e-106">屬性集是由 [**controlAccessRight**](/windows/desktop/ADSchema/c-controlaccessright)物件之 [**rightsGUID**](/windows/desktop/ADSchema/a-rightsguid)屬性中的 GUID 所識別。</span><span class="sxs-lookup"><span data-stu-id="d478e-106">A property set is identified by the GUID in the [**rightsGUID**](/windows/desktop/ADSchema/a-rightsguid) attribute of a [**controlAccessRight**](/windows/desktop/ADSchema/c-controlaccessright) object.</span></span> <span data-ttu-id="d478e-107">此 GUID 是在群組中每個屬性之 [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema)物件的 [**attributeSecurityGUID**](/windows/desktop/ADSchema/a-attributesecurityguid)屬性中設定。</span><span class="sxs-lookup"><span data-stu-id="d478e-107">This GUID is set in the [**attributeSecurityGUID**](/windows/desktop/ADSchema/a-attributesecurityguid) attribute of the [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object of each attribute in the group.</span></span>

<span data-ttu-id="d478e-108">下列程式示範如何設定適用于物件屬性群組的許可權。</span><span class="sxs-lookup"><span data-stu-id="d478e-108">The following procedure shows how to set permissions that apply to a group of object properties.</span></span>

<span data-ttu-id="d478e-109">**若要設定適用于物件屬性群組的許可權**</span><span class="sxs-lookup"><span data-stu-id="d478e-109">**To set permissions that apply to a group of object properties**</span></span>

1.  <span data-ttu-id="d478e-110">將 [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性設定為 [ **ads \_ right \_ ds \_ 讀取 \_**] 屬性、[ **廣告正確的 \_ \_ ds \_ 寫入 \_** ] 屬性或兩個 [值] 組合。</span><span class="sxs-lookup"><span data-stu-id="d478e-110">Set the [**IADsAccessControlEntry.AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_RIGHT\_DS\_READ\_PROP**, **ADS\_RIGHT\_DS\_WRITE\_PROP** or both values combined.</span></span>
2.  <span data-ttu-id="d478e-111">將 [**IADsAccessControlEntry AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性設定為 **ADS \_ AceType \_ 存取允許的 \_ \_ 物件** 或 **ads \_ AceType \_ 拒絕存取 \_ \_ 物件**。</span><span class="sxs-lookup"><span data-stu-id="d478e-111">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to either **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
3.  <span data-ttu-id="d478e-112">將 [ [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) ] 屬性設定為屬性集的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d478e-112">Set the [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the GUID of the property set.</span></span> <span data-ttu-id="d478e-113">這是識別屬性集之 [**controlAccessRight**](/windows/desktop/ADSchema/c-controlaccessright)物件的 [**rightsGUID**](/windows/desktop/ADSchema/a-rightsguid)屬性。</span><span class="sxs-lookup"><span data-stu-id="d478e-113">This is the [**rightsGUID**](/windows/desktop/ADSchema/a-rightsguid) property of the [**controlAccessRight**](/windows/desktop/ADSchema/c-controlaccessright) object that identifies the property set.</span></span> <span data-ttu-id="d478e-114">此 GUID 也會設定為群組中每個屬性之 attributeSchema 物件的 [**attributeSecurityGUID**](/windows/desktop/ADSchema/a-attributesecurityguid) 。</span><span class="sxs-lookup"><span data-stu-id="d478e-114">This GUID is also set as the [**attributeSecurityGUID**](/windows/desktop/ADSchema/a-attributesecurityguid) in the attributeSchema object of each property in the group.</span></span>
4.  <span data-ttu-id="d478e-115">將 [ [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) ] 屬性設定為 [ **ADS \_ 旗標 \_ 物件 \_ 類型 \_**]。</span><span class="sxs-lookup"><span data-stu-id="d478e-115">Set the [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT**.</span></span>

<span data-ttu-id="d478e-116">請注意，您不應該在 [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods)屬性中設定 **ADS 的 \_ 正確 \_ DS \_ 控制 \_ 存取** 旗標。</span><span class="sxs-lookup"><span data-stu-id="d478e-116">Be aware that you should not set the **ADS\_RIGHT\_DS\_CONTROL\_ACCESS** flag in the [**IADsAccessControlEntry.AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property.</span></span> <span data-ttu-id="d478e-117">此旗標只會用來指定控制項存取權限。</span><span class="sxs-lookup"><span data-stu-id="d478e-117">This flag is only used to specify a control access right.</span></span>

<span data-ttu-id="d478e-118">如需可用於設定屬性集之存取權限的詳細資訊和程式碼範例，請參閱 [設定屬性群組許可權的範例程式碼](example-code-for-setting-permissions-on-a-group-of-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="d478e-118">For more information and a code example that can be used to set access rights for a property set, see [Example Code for Setting Permissions on a Group of Properties](example-code-for-setting-permissions-on-a-group-of-properties.md).</span></span>

<span data-ttu-id="d478e-119">如需建立 ACE 的詳細資訊，請參閱 [設定物件的存取權限](setting-access-rights-on-an-object.md)。</span><span class="sxs-lookup"><span data-stu-id="d478e-119">For more information about creating an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="d478e-120">如需可用於設定屬性集之 ACE 的詳細資訊和程式碼範例，請參閱 [在目錄物件上設定 ace 的範例程式碼](example-code-for-setting-an-ace-on-a-directory-object.md)。</span><span class="sxs-lookup"><span data-stu-id="d478e-120">For more information and a code example that can be used to set an ACE for a property set, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 