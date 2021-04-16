---
description: 與 NCRYPT \_ UI \_ 原則 \_ 屬性屬性搭配使用，以包含索引鍵的使用者介面資訊。
ms.assetid: c567d8ba-3315-4316-8e09-93b2c10a55ec
title: 'NCRYPT_UI_POLICY_BLOB 結構 (Ncrypt \_ provider .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NCRYPT_UI_POLICY_BLOB
api_type:
- HeaderDef
api_location:
- Ncrypt_provider.h
ms.openlocfilehash: c45b53e051f021ab3dcce6dab4e2317572338624
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513145"
---
# <a name="ncrypt_ui_policy_blob-structure"></a><span data-ttu-id="cac94-103">NCRYPT \_ UI \_ 原則 \_ BLOB 結構</span><span class="sxs-lookup"><span data-stu-id="cac94-103">NCRYPT\_UI\_POLICY\_BLOB structure</span></span>

<span data-ttu-id="cac94-104">**NCRYPT \_ ui \_ 原則 \_ BLOB** 結構會與 [**NCRYPT \_ ui \_ 原則 \_ 屬性**](key-storage-property-identifiers.md)屬性搭配使用，以包含金鑰的使用者介面資訊。</span><span class="sxs-lookup"><span data-stu-id="cac94-104">The **NCRYPT\_UI\_POLICY\_BLOB** structure is used with the [**NCRYPT\_UI\_POLICY\_PROPERTY**](key-storage-property-identifiers.md) property to contain user interface information for a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="cac94-105">語法</span><span class="sxs-lookup"><span data-stu-id="cac94-105">Syntax</span></span>


```C++
typedef struct __NCRYPT_UI_POLICY_BLOB {
  DWORD dwVersion;
  DWORD dwFlags;
  DWORD cbCreationTitle;
  DWORD cbFriendlyName;
  DWORD cbDescription;
} NCRYPT_UI_POLICY_BLOB;
```



## <a name="members"></a><span data-ttu-id="cac94-106">成員</span><span class="sxs-lookup"><span data-stu-id="cac94-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cac94-107">**dwVersion**</span><span class="sxs-lookup"><span data-stu-id="cac94-107">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="cac94-108">結構的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="cac94-108">The version number of the structure.</span></span> <span data-ttu-id="cac94-109">此成員必須包含1。</span><span class="sxs-lookup"><span data-stu-id="cac94-109">This member must contain 1.</span></span>

</dd> <dt>

<span data-ttu-id="cac94-110">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="cac94-110">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="cac94-111">一組旗標，可提供額外的使用者介面資訊或需求。</span><span class="sxs-lookup"><span data-stu-id="cac94-111">A set of flags that provide additional user interface information or requirements.</span></span>



| <span data-ttu-id="cac94-112">值</span><span class="sxs-lookup"><span data-stu-id="cac94-112">Value</span></span>                                                                                                                                                                                                                                                                                                  | <span data-ttu-id="cac94-113">意義</span><span class="sxs-lookup"><span data-stu-id="cac94-113">Meaning</span></span>                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="NCRYPT_UI_PROTECT_KEY_FLAG"></span><span id="ncrypt_ui_protect_key_flag"></span><dl> <span data-ttu-id="cac94-114"><dt>**NCRYPT \_UI \_ 保護 \_ 金鑰 \_ 旗**</dt>標 <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="cac94-114"><dt>**NCRYPT\_UI\_PROTECT\_KEY\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl>                                | <span data-ttu-id="cac94-115">視需要顯示強式金鑰使用者介面。</span><span class="sxs-lookup"><span data-stu-id="cac94-115">Display the strong key user interface as needed.</span></span><br/> |
| <span id="NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG"></span><span id="ncrypt_ui_force_high_protection_flag"></span><dl> <span data-ttu-id="cac94-116"><dt>**NCRYPT \_UI \_ 強制 \_ 高 \_ 保護 \_ 旗**</dt>標 <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="cac94-116"><dt>**NCRYPT\_UI\_FORCE\_HIGH\_PROTECTION\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="cac94-117">強制執行高保護。</span><span class="sxs-lookup"><span data-stu-id="cac94-117">Force high protection.</span></span><br/>                           |



 

</dd> <dt>

<span data-ttu-id="cac94-118">**cbCreationTitle**</span><span class="sxs-lookup"><span data-stu-id="cac94-118">**cbCreationTitle**</span></span>
</dt> <dd>

<span data-ttu-id="cac94-119">建立標題的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cac94-119">The length, in bytes, of the creation title.</span></span> <span data-ttu-id="cac94-120">建立標題是以 null 結束的 Unicode 字串，它會指定當索引鍵完成時，用來做為 [強式索引鍵] 對話方塊標題的文字。</span><span class="sxs-lookup"><span data-stu-id="cac94-120">The creation title is a null-terminated Unicode string that specifies the text that is used as the title of the strong key dialog box when the key is completed.</span></span> <span data-ttu-id="cac94-121">建立標題必須緊接在 **NCRYPT \_ UI \_ 原則 \_ BLOB** 結構之後。</span><span class="sxs-lookup"><span data-stu-id="cac94-121">The creation title must be placed immediately following the **NCRYPT\_UI\_POLICY\_BLOB** structure.</span></span> <span data-ttu-id="cac94-122">如果 **cbCreationTitle** 成員的值設定為0，則會使用預設建立標題作為 [強式索引鍵] 對話方塊的標題。</span><span class="sxs-lookup"><span data-stu-id="cac94-122">If the value of the **cbCreationTitle** member is set to 0, a default creation title is used for the title of the strong key dialog box.</span></span> <span data-ttu-id="cac94-123">只有在金鑰完成時才會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="cac94-123">This member is only used on key finalization.</span></span>

</dd> <dt>

<span data-ttu-id="cac94-124">**cbFriendlyName**</span><span class="sxs-lookup"><span data-stu-id="cac94-124">**cbFriendlyName**</span></span>
</dt> <dd>

<span data-ttu-id="cac94-125">金鑰的易記名稱長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cac94-125">The length, in bytes, of the friendly name of the key.</span></span> <span data-ttu-id="cac94-126">易記名稱是以 null 結束的 Unicode 字串，其中包含 [強式索引鍵] 對話方塊中顯示的文字作為索引鍵的名稱。</span><span class="sxs-lookup"><span data-stu-id="cac94-126">The friendly name is a null-terminated Unicode string that contains the text that is displayed in the strong key dialog box as the name of the key.</span></span> <span data-ttu-id="cac94-127">易記名稱必須緊接在此 BLOB 中的建立標題之後。</span><span class="sxs-lookup"><span data-stu-id="cac94-127">The friendly name must be placed immediately following the creation title in this BLOB.</span></span> <span data-ttu-id="cac94-128">如果 **cbFriendlyName** 成員的值設定為0，就會在 [強式索引鍵] 對話方塊中使用預設名稱。</span><span class="sxs-lookup"><span data-stu-id="cac94-128">If the value of the **cbFriendlyName** member is set to 0, a default name is used in the strong key dialog box.</span></span> <span data-ttu-id="cac94-129">當金鑰完成和使用金鑰時，都會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="cac94-129">This member is used both when the key is completed and when the key is used.</span></span>

</dd> <dt>

<span data-ttu-id="cac94-130">**cbDescription**</span><span class="sxs-lookup"><span data-stu-id="cac94-130">**cbDescription**</span></span>
</dt> <dd>

<span data-ttu-id="cac94-131">金鑰描述的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cac94-131">The length, in bytes, of the key description.</span></span> <span data-ttu-id="cac94-132">金鑰描述是以 null 結束的 Unicode 字串，其中包含 [強式索引鍵] 對話方塊中顯示的文字作為索引鍵的描述。</span><span class="sxs-lookup"><span data-stu-id="cac94-132">The key description is a null-terminated Unicode string that contains the text that is displayed in the strong key dialog box as the description of the key.</span></span> <span data-ttu-id="cac94-133">描述值必須緊接在此 BLOB 中的易記名稱之後。</span><span class="sxs-lookup"><span data-stu-id="cac94-133">The description value must be placed immediately following the friendly name in this BLOB.</span></span> <span data-ttu-id="cac94-134">如果 **cbDescription** 成員的值設定為0，就會在 [強式索引鍵] 對話方塊中使用預設描述。</span><span class="sxs-lookup"><span data-stu-id="cac94-134">If the value of the **cbDescription** member is set to 0, a default description is used in the strong key dialog box.</span></span> <span data-ttu-id="cac94-135">當金鑰完成和使用金鑰時，都會使用這個成員。</span><span class="sxs-lookup"><span data-stu-id="cac94-135">This member is used both when the key is completed and when the key is used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cac94-136">備註</span><span class="sxs-lookup"><span data-stu-id="cac94-136">Remarks</span></span>

<span data-ttu-id="cac94-137">此結構包含在 Ncrypt \_ 提供者 .h 標頭中。</span><span class="sxs-lookup"><span data-stu-id="cac94-137">This structure is included in the Ncrypt\_provider.h header.</span></span> <span data-ttu-id="cac94-138">若要使用此結構，您必須從 Microsoft Connect 下載 [密碼編譯提供者開發工具組](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) 。</span><span class="sxs-lookup"><span data-stu-id="cac94-138">To use the structure, you must download the [Cryptographic Provider Development Kit](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) from Microsoft Connect.</span></span>

## <a name="requirements"></a><span data-ttu-id="cac94-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="cac94-139">Requirements</span></span>



| <span data-ttu-id="cac94-140">需求</span><span class="sxs-lookup"><span data-stu-id="cac94-140">Requirement</span></span> | <span data-ttu-id="cac94-141">值</span><span class="sxs-lookup"><span data-stu-id="cac94-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cac94-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cac94-142">Minimum supported client</span></span><br/> | <span data-ttu-id="cac94-143">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cac94-143">Windows Vista \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cac94-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cac94-144">Minimum supported server</span></span><br/> | <span data-ttu-id="cac94-145">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cac94-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cac94-146">標頭</span><span class="sxs-lookup"><span data-stu-id="cac94-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="cac94-147"><dt>Ncrypt \_ provider。h</dt></span><span class="sxs-lookup"><span data-stu-id="cac94-147"><dt>Ncrypt\_provider.h</dt></span></span> </dl> |



 

