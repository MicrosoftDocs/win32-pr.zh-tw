---
description: 用來設定 CAPICOM 元件。
title: Settings 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 27042f9602167f3eb0c1272f7c19fa1170abab40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998630"
---
# <a name="settings-object-cryptography"></a><span data-ttu-id="41b96-103">設定物件 (密碼編譯) </span><span class="sxs-lookup"><span data-stu-id="41b96-103">Settings object (Cryptography)</span></span>

<span data-ttu-id="41b96-104">\[[ **設定** ] 物件可用於 [需求] 區段中指定的作業系統。\]</span><span class="sxs-lookup"><span data-stu-id="41b96-104">\[The **Settings** object is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="41b96-105">**Settings** 物件是用來設定 CAPICOM 元件。</span><span class="sxs-lookup"><span data-stu-id="41b96-105">The **Settings** object is used to configure CAPICOM components.</span></span>

## <a name="members"></a><span data-ttu-id="41b96-106">成員</span><span class="sxs-lookup"><span data-stu-id="41b96-106">Members</span></span>

<span data-ttu-id="41b96-107">**Settings** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="41b96-107">The **Settings** object has these types of members:</span></span>

-   [<span data-ttu-id="41b96-108">屬性</span><span class="sxs-lookup"><span data-stu-id="41b96-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="41b96-109">屬性</span><span class="sxs-lookup"><span data-stu-id="41b96-109">Properties</span></span>

<span data-ttu-id="41b96-110">**Settings** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="41b96-110">The **Settings** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="41b96-111">屬性</span><span class="sxs-lookup"><span data-stu-id="41b96-111">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="41b96-112">存取類型</span><span class="sxs-lookup"><span data-stu-id="41b96-112">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="41b96-113">Description</span><span class="sxs-lookup"><span data-stu-id="41b96-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="41b96-114"><a href="settings-activedirectorysearchlocation.md"><strong>ActiveDirectorySearchLocation</strong></a></span><span class="sxs-lookup"><span data-stu-id="41b96-114"><a href="settings-activedirectorysearchlocation.md"><strong>ActiveDirectorySearchLocation</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="41b96-115">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="41b96-115">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="41b96-116">設定或抓取 Active Directory 搜尋位置。</span><span class="sxs-lookup"><span data-stu-id="41b96-116">Sets or retrieves the Active Directory search location.</span></span> <span data-ttu-id="41b96-117">預設不會指定初始位置。</span><span class="sxs-lookup"><span data-stu-id="41b96-117">The initial location is unspecified by default.</span></span> <span data-ttu-id="41b96-118">如果未指定位置，則會搜尋通用類別目錄，然後搜尋預設網域。</span><span class="sxs-lookup"><span data-stu-id="41b96-118">When the location is unspecified, the global catalog is searched, then the default domain is searched.</span></span> <span data-ttu-id="41b96-119">搜尋會判斷使用者憑證屬性是否在該位置發佈。</span><span class="sxs-lookup"><span data-stu-id="41b96-119">The search determines whether the user certificate attribute is published at that location.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="41b96-120"><a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a></span><span class="sxs-lookup"><span data-stu-id="41b96-120"><a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="41b96-121">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="41b96-121">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="41b96-122">設定或取得布林值，這個值會指出是否可以使用使用者介面提示輸入簽署者或寄件者的身分識別。</span><span class="sxs-lookup"><span data-stu-id="41b96-122">Sets or retrieves a Boolean value that indicates whether user interface prompts for a signer or sender's identity can be used.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="41b96-123">設定這個屬性並不會停用從 web 應用程式完成任何私密金鑰使用之前所產生的警告。</span><span class="sxs-lookup"><span data-stu-id="41b96-123">Setting this property does not disable warnings that are generated before any private key usage is done from a web-based application.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="41b96-124">備註</span><span class="sxs-lookup"><span data-stu-id="41b96-124">Remarks</span></span>

<span data-ttu-id="41b96-125">您可以建立 **設定** 物件，而且可以安全地進行腳本處理。</span><span class="sxs-lookup"><span data-stu-id="41b96-125">The **Settings** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="41b96-126">**Settings** 物件的 PROGID 是 CAPICOM。設定。1。</span><span class="sxs-lookup"><span data-stu-id="41b96-126">The ProgID for the **Settings** object is CAPICOM.Settings.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="41b96-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="41b96-127">Requirements</span></span>



| <span data-ttu-id="41b96-128">需求</span><span class="sxs-lookup"><span data-stu-id="41b96-128">Requirement</span></span> | <span data-ttu-id="41b96-129">值</span><span class="sxs-lookup"><span data-stu-id="41b96-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41b96-130">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="41b96-130">Redistributable</span></span><br/> | <span data-ttu-id="41b96-131">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="41b96-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="41b96-132">DLL</span><span class="sxs-lookup"><span data-stu-id="41b96-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="41b96-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41b96-133"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41b96-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41b96-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41b96-135">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="41b96-135">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 




