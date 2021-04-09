---
description: CIM \_ SupportAccess 類別定義了如何取得產品的協助。
ms.assetid: f42a793f-d71e-498e-9c6b-581aa029a0dd
ms.tgt_platform: multiple
title: CIM_SupportAccess 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SupportAccess
- CIM_SupportAccess.CommunicationInfo
- CIM_SupportAccess.CommunicationMode
- CIM_SupportAccess.Description
- CIM_SupportAccess.Locale
- CIM_SupportAccess.SupportAccessId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: db5f1dc4331bd50e2fc61899f9d45fe2cdb0eca0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110756"
---
# <a name="cim_supportaccess-class"></a><span data-ttu-id="a3aab-103">CIM \_ SupportAccess 類別</span><span class="sxs-lookup"><span data-stu-id="a3aab-103">CIM\_SupportAccess class</span></span>

<span data-ttu-id="a3aab-104">**CIM \_ SupportAccess** 類別定義了如何取得產品的協助。</span><span class="sxs-lookup"><span data-stu-id="a3aab-104">The **CIM\_SupportAccess** class defines how to obtain assistance for a product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a3aab-105">DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。</span><span class="sxs-lookup"><span data-stu-id="a3aab-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a3aab-106">WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。</span><span class="sxs-lookup"><span data-stu-id="a3aab-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a3aab-107">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="a3aab-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a3aab-108">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="a3aab-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3aab-109">語法</span><span class="sxs-lookup"><span data-stu-id="a3aab-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{80321714-DB31-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_SupportAccess
{
  string CommunicationInfo;
  uint16 CommunicationMode;
  string Description;
  string Locale;
  string SupportAccessId;
};
```

## <a name="members"></a><span data-ttu-id="a3aab-110">成員</span><span class="sxs-lookup"><span data-stu-id="a3aab-110">Members</span></span>

<span data-ttu-id="a3aab-111">**CIM \_ SupportAccess** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="a3aab-111">The **CIM\_SupportAccess** class has these types of members:</span></span>

-   [<span data-ttu-id="a3aab-112">屬性</span><span class="sxs-lookup"><span data-stu-id="a3aab-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a3aab-113">屬性</span><span class="sxs-lookup"><span data-stu-id="a3aab-113">Properties</span></span>

<span data-ttu-id="a3aab-114">**CIM \_ SupportAccess** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="a3aab-114">The **CIM\_SupportAccess** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a3aab-115">**CommunicationInfo**</span><span class="sxs-lookup"><span data-stu-id="a3aab-115">**CommunicationInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3aab-116">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a3aab-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3aab-117">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a3aab-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3aab-118">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| FRU \| 002.11 "，" MIF。DMTF \| FRU \| 002.12」 ) </span><span class="sxs-lookup"><span data-stu-id="a3aab-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.11", "MIF.DMTF\|FRU\|002.12")</span></span>
</dt> </dl>

<span data-ttu-id="a3aab-119">通訊模式的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a3aab-119">Details of the communication mode.</span></span> <span data-ttu-id="a3aab-120">例如，如果 **CommunicationMode** 屬性是 "Phone"，則此屬性會指定要呼叫的電話號碼。</span><span class="sxs-lookup"><span data-stu-id="a3aab-120">For example, if the **CommunicationMode** property is "Phone", then this property specifies the phone number to call.</span></span>

</dd> <dt>

<span data-ttu-id="a3aab-121">**CommunicationMode**</span><span class="sxs-lookup"><span data-stu-id="a3aab-121">**CommunicationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3aab-122">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="a3aab-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a3aab-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a3aab-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3aab-124">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 支援 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="a3aab-124">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="a3aab-125">用來取得支援的通訊形式。</span><span class="sxs-lookup"><span data-stu-id="a3aab-125">Form of communication to use to obtain support.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a3aab-126"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) </span><span class="sxs-lookup"><span data-stu-id="a3aab-126"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>

<span data-ttu-id="a3aab-127"><span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>**Phone** (2) </span><span class="sxs-lookup"><span data-stu-id="a3aab-127"><span id="Phone"></span><span id="phone"></span><span id="PHONE"></span>**Phone** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Fax"></span><span id="fax"></span><span id="FAX"></span>

<span data-ttu-id="a3aab-128"><span id="Fax"></span><span id="fax"></span><span id="FAX"></span>**傳真** (3) </span><span class="sxs-lookup"><span data-stu-id="a3aab-128"><span id="Fax"></span><span id="fax"></span><span id="FAX"></span>**Fax** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="BBS"></span><span id="bbs"></span>

<span data-ttu-id="a3aab-129"><span id="BBS"></span><span id="bbs"></span>**BBS** (4) </span><span class="sxs-lookup"><span data-stu-id="a3aab-129"><span id="BBS"></span><span id="bbs"></span>**BBS** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>

<span data-ttu-id="a3aab-130"><span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>**線上服務** (5) </span><span class="sxs-lookup"><span data-stu-id="a3aab-130"><span id="Online_Service"></span><span id="online_service"></span><span id="ONLINE_SERVICE"></span>**Online Service** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>

<span data-ttu-id="a3aab-131"><span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>**網頁** (6) </span><span class="sxs-lookup"><span data-stu-id="a3aab-131"><span id="Web_Page"></span><span id="web_page"></span><span id="WEB_PAGE"></span>**Web Page** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a3aab-132">網頁</span><span class="sxs-lookup"><span data-stu-id="a3aab-132">Webpage</span></span>

</dd> <dt>

<span id="FTP"></span><span id="ftp"></span>

<span data-ttu-id="a3aab-133"><span id="FTP"></span><span id="ftp"></span>**FTP** (7) </span><span class="sxs-lookup"><span data-stu-id="a3aab-133"><span id="FTP"></span><span id="ftp"></span>**FTP** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>

<span data-ttu-id="a3aab-134"><span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>**電子郵件** (8) </span><span class="sxs-lookup"><span data-stu-id="a3aab-134"><span id="E-mail"></span><span id="e-mail"></span><span id="E-MAIL"></span>**E-mail** (8)</span></span>


</dt> <dd>

<span data-ttu-id="a3aab-135">電子郵件</span><span class="sxs-lookup"><span data-stu-id="a3aab-135">Email</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a3aab-136">**說明**</span><span class="sxs-lookup"><span data-stu-id="a3aab-136">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3aab-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a3aab-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3aab-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a3aab-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3aab-139">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 支援 \| 001.3 ") </span><span class="sxs-lookup"><span data-stu-id="a3aab-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="a3aab-140">提供之支援類型的文字描述。</span><span class="sxs-lookup"><span data-stu-id="a3aab-140">Textual description of the type of support provided.</span></span>

</dd> <dt>

<span data-ttu-id="a3aab-141">**地區設定**</span><span class="sxs-lookup"><span data-stu-id="a3aab-141">**Locale**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3aab-142">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a3aab-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3aab-143">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a3aab-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3aab-144">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 支援 \| 001.2 ") ， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="a3aab-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Support\|001.2"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a3aab-145">此支援資源適用的地理區域或語言方言。</span><span class="sxs-lookup"><span data-stu-id="a3aab-145">Geographic region or language dialect to which this support resource pertains.</span></span>

</dd> <dt>

<span data-ttu-id="a3aab-146">**SupportAccessId**</span><span class="sxs-lookup"><span data-stu-id="a3aab-146">**SupportAccessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3aab-147">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="a3aab-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a3aab-148">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="a3aab-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3aab-149">限定詞： [**Key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) </span><span class="sxs-lookup"><span data-stu-id="a3aab-149">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a3aab-150">由產品廠商或部署產品的組織所定義的任意自由格式字串。</span><span class="sxs-lookup"><span data-stu-id="a3aab-150">Arbitrary free-form string defined by the product vendor or by the organization that deploys the product.</span></span> <span data-ttu-id="a3aab-151">由於這個屬性是索引鍵，因此在整個企業中都必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="a3aab-151">This property, since it is a key, should be unique throughout the enterprise.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3aab-152">備註</span><span class="sxs-lookup"><span data-stu-id="a3aab-152">Remarks</span></span>

<span data-ttu-id="a3aab-153">WMI 不會執行這個類別。</span><span class="sxs-lookup"><span data-stu-id="a3aab-153">WMI does not implement this class.</span></span>

<span data-ttu-id="a3aab-154">此檔衍生自 DMTF 所發佈的 CIM 類別描述。</span><span class="sxs-lookup"><span data-stu-id="a3aab-154">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a3aab-155">Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="a3aab-155">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3aab-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="a3aab-156">Requirements</span></span>



| <span data-ttu-id="a3aab-157">需求</span><span class="sxs-lookup"><span data-stu-id="a3aab-157">Requirement</span></span> | <span data-ttu-id="a3aab-158">值</span><span class="sxs-lookup"><span data-stu-id="a3aab-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a3aab-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a3aab-159">Minimum supported client</span></span><br/> | <span data-ttu-id="a3aab-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3aab-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a3aab-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a3aab-161">Minimum supported server</span></span><br/> | <span data-ttu-id="a3aab-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3aab-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a3aab-163">命名空間</span><span class="sxs-lookup"><span data-stu-id="a3aab-163">Namespace</span></span><br/>                | <span data-ttu-id="a3aab-164">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a3aab-164">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a3aab-165">MOF</span><span class="sxs-lookup"><span data-stu-id="a3aab-165">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3aab-166"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3aab-166"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3aab-167">DLL</span><span class="sxs-lookup"><span data-stu-id="a3aab-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3aab-168"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a3aab-168"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

