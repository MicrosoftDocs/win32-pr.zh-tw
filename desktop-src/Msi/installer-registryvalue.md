---
description: 安裝程式物件的 RegistryValue 方法會讀取指定之登錄機碼值的相關資訊。
ms.assetid: 63c258f9-8649-419d-9f79-3681f9f97302
title: 安裝程式. RegistryValue 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RegistryValue
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6da79ff08eebe62ad177119a35bfc29b21c9350
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989651"
---
# <a name="installerregistryvalue-method"></a><span data-ttu-id="41205-103">安裝程式. RegistryValue 方法</span><span class="sxs-lookup"><span data-stu-id="41205-103">Installer.RegistryValue method</span></span>

<span data-ttu-id="41205-104">[**安裝程式**](installer-object.md)物件的 **RegistryValue** 方法會讀取指定之登錄機碼值的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="41205-104">The **RegistryValue** method of the [**Installer**](installer-object.md) object reads information about a specified registry key of value.</span></span> <span data-ttu-id="41205-105">如果指定的索引鍵或值不存在，此方法會傳回9的錯誤：「下標超出範圍」。</span><span class="sxs-lookup"><span data-stu-id="41205-105">If the key or value specified does not exist, the method returns an error of 9, "Subscript out of Range."</span></span>

## <a name="syntax"></a><span data-ttu-id="41205-106">語法</span><span class="sxs-lookup"><span data-stu-id="41205-106">Syntax</span></span>


```JScript
Installer.RegistryValue(
  root,
  key,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="41205-107">參數</span><span class="sxs-lookup"><span data-stu-id="41205-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41205-108">*root*</span><span class="sxs-lookup"><span data-stu-id="41205-108">*root*</span></span> 
</dt> <dd>

<span data-ttu-id="41205-109">在 Windows NT 4.0 中，登錄根目錄為數字根金鑰或電腦名稱稱，表示為字串。</span><span class="sxs-lookup"><span data-stu-id="41205-109">In Windows NT 4.0, the registry root is either a numeric root key or a machine name as a string.</span></span> <span data-ttu-id="41205-110">電腦名稱稱一律為字串。</span><span class="sxs-lookup"><span data-stu-id="41205-110">Machine names are always strings.</span></span> <span data-ttu-id="41205-111">在 Windows 95、Windows 98 或 Windows Me 中，登錄根目錄只是數位的根機碼。</span><span class="sxs-lookup"><span data-stu-id="41205-111">In Windows 95, Windows 98, or Windows Me, the registry root is a numeric root key only.</span></span> <span data-ttu-id="41205-112">您只能存取遠端電腦上的 HKLM。</span><span class="sxs-lookup"><span data-stu-id="41205-112">You can only access HKLM on a remote machine.</span></span>



| <span data-ttu-id="41205-113">Root</span><span class="sxs-lookup"><span data-stu-id="41205-113">Root</span></span>                                                                                                                                                                                   | <span data-ttu-id="41205-114">意義</span><span class="sxs-lookup"><span data-stu-id="41205-114">Meaning</span></span>      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span id="HKEY_CLASSES_ROOT"></span><span id="hkey_classes_root"></span><dl> <span data-ttu-id="41205-115"><dt>**HKEY \_ 類別 \_ 根目錄**</dt></span><span class="sxs-lookup"><span data-stu-id="41205-115"><dt>**HKEY\_CLASSES\_ROOT**</dt></span></span> </dl>             | <span data-ttu-id="41205-116">0</span><span class="sxs-lookup"><span data-stu-id="41205-116">0</span></span><br/> |
| <span id="HKEY_CURRENT_USER"></span><span id="hkey_current_user"></span><dl> <span data-ttu-id="41205-117"><dt>**HKEY \_ 目前的 \_ 使用者**</dt></span><span class="sxs-lookup"><span data-stu-id="41205-117"><dt>**HKEY\_CURRENT\_USER**</dt></span></span> </dl>             | <span data-ttu-id="41205-118">1</span><span class="sxs-lookup"><span data-stu-id="41205-118">1</span></span><br/> |
| <span id="HKEY_LOCAL_MACHINE"></span><span id="hkey_local_machine"></span><dl> <span data-ttu-id="41205-119"><dt>**HKEY \_ 本機 \_ 電腦**</dt></span><span class="sxs-lookup"><span data-stu-id="41205-119"><dt>**HKEY\_LOCAL\_MACHINE**</dt></span></span> </dl>          | <span data-ttu-id="41205-120">2</span><span class="sxs-lookup"><span data-stu-id="41205-120">2</span></span><br/> |
| <span id="HKEY_USERS"></span><span id="hkey_users"></span><dl> <span data-ttu-id="41205-121"><dt>**HKEY \_ 使用者**</dt></span><span class="sxs-lookup"><span data-stu-id="41205-121"><dt>**HKEY\_USERS**</dt></span></span> </dl>                                   | <span data-ttu-id="41205-122">3</span><span class="sxs-lookup"><span data-stu-id="41205-122">3</span></span><br/> |
| <span id="HKEY_PERFORMANCE_DATA"></span><span id="hkey_performance_data"></span><dl> <span data-ttu-id="41205-123"><dt>**HKEY \_ 效能 \_ 資料**</dt></span><span class="sxs-lookup"><span data-stu-id="41205-123"><dt>**HKEY\_PERFORMANCE\_DATA**</dt></span></span> </dl> | <span data-ttu-id="41205-124">4</span><span class="sxs-lookup"><span data-stu-id="41205-124">4</span></span><br/> |
| <span id="HKEY_CURRENT_CONFIG"></span><span id="hkey_current_config"></span><dl> <span data-ttu-id="41205-125"><dt>**HKEY \_ 目前的設定 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="41205-125"><dt>**HKEY\_CURRENT\_CONFIG**</dt></span></span> </dl>       | <span data-ttu-id="41205-126">5</span><span class="sxs-lookup"><span data-stu-id="41205-126">5</span></span><br/> |
| <span id="HKEY_DYN_DATA"></span><span id="hkey_dyn_data"></span><dl> <span data-ttu-id="41205-127"><dt>**HKEY \_ DYN \_ 資料**</dt></span><span class="sxs-lookup"><span data-stu-id="41205-127"><dt>**HKEY\_DYN\_DATA**</dt></span></span> </dl>                         | <span data-ttu-id="41205-128">6</span><span class="sxs-lookup"><span data-stu-id="41205-128">6</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="41205-129">*key*</span><span class="sxs-lookup"><span data-stu-id="41205-129">*key*</span></span> 
</dt> <dd>

<span data-ttu-id="41205-130">字串，包含來自根目錄的完整索引鍵路徑。</span><span class="sxs-lookup"><span data-stu-id="41205-130">A string containing the complete key path from the root.</span></span>

</dd> <dt>

<span data-ttu-id="41205-131">*value*</span><span class="sxs-lookup"><span data-stu-id="41205-131">*value*</span></span> 
</dt> <dd>

<span data-ttu-id="41205-132">這個選擇性參數會指定要針對指定的索引鍵傳回的關聯值。</span><span class="sxs-lookup"><span data-stu-id="41205-132">This optional parameter designates which associated value to return for the specified key.</span></span> <span data-ttu-id="41205-133">值是下表所示的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="41205-133">The value is one of the values shown in the following table.</span></span>



| <span data-ttu-id="41205-134">值</span><span class="sxs-lookup"><span data-stu-id="41205-134">Value</span></span>                                                                                                                                                                                                    | <span data-ttu-id="41205-135">意義</span><span class="sxs-lookup"><span data-stu-id="41205-135">Meaning</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Missing_or_blank"></span><span id="missing_or_blank"></span><span id="MISSING_OR_BLANK"></span><dl> <span data-ttu-id="41205-136"><dt>**遺漏或空白**</dt></span><span class="sxs-lookup"><span data-stu-id="41205-136"><dt>**Missing or blank**</dt></span></span> </dl> | <span data-ttu-id="41205-137">傳回布林值，指定索引鍵是否存在。</span><span class="sxs-lookup"><span data-stu-id="41205-137">Returns a Boolean designating whether the key exists.</span></span><br/>                                                                                        |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <span data-ttu-id="41205-138"><dt>**字串**</dt></span><span class="sxs-lookup"><span data-stu-id="41205-138"><dt>**String**</dt></span></span> </dl>                                         | <span data-ttu-id="41205-139">如果值名稱不存在，則會傳回與所指定值相關聯的資料。</span><span class="sxs-lookup"><span data-stu-id="41205-139">Returns the data associated with the named value, fails if the value name is non-existent.</span></span><br/>                                                   |
| <span id="Positive_integer"></span><span id="positive_integer"></span><span id="POSITIVE_INTEGER"></span><dl> <span data-ttu-id="41205-140"><dt>**正整數**</dt></span><span class="sxs-lookup"><span data-stu-id="41205-140"><dt>**Positive integer**</dt></span></span> </dl> | <span data-ttu-id="41205-141">傳回以1為基礎的列舉值名稱，如果不存在，則會是空的。</span><span class="sxs-lookup"><span data-stu-id="41205-141">Returns the 1-based enumerated value name, it is empty if non-existent.</span></span> <span data-ttu-id="41205-142">此選項會使用 [**RegEnumValue**](/windows/win32/api/winreg/nf-winreg-regenumvaluea) 函數。</span><span class="sxs-lookup"><span data-stu-id="41205-142">This option uses the [**RegEnumValue**](/windows/win32/api/winreg/nf-winreg-regenumvaluea) function.</span></span><br/> |
| <span id="Negative_integer"></span><span id="negative_integer"></span><span id="NEGATIVE_INTEGER"></span><dl> <span data-ttu-id="41205-143"><dt>**負整數**</dt></span><span class="sxs-lookup"><span data-stu-id="41205-143"><dt>**Negative integer**</dt></span></span> </dl> | <span data-ttu-id="41205-144">傳回以1為基礎的列舉子機碼名稱，如果不存在，則為空白。</span><span class="sxs-lookup"><span data-stu-id="41205-144">Returns the 1-based enumerated subkey name, this is empty if non-existent.</span></span> <span data-ttu-id="41205-145">此選項會使用 [**RegEnumKey**](/windows/win32/api/winreg/nf-winreg-regenumkeya) 函數。</span><span class="sxs-lookup"><span data-stu-id="41205-145">This option uses the [**RegEnumKey**](/windows/win32/api/winreg/nf-winreg-regenumkeya) function.</span></span><br/>  |
| <span id="Zero_integer"></span><span id="zero_integer"></span><span id="ZERO_INTEGER"></span><dl> <span data-ttu-id="41205-146"><dt>**零整數**</dt></span><span class="sxs-lookup"><span data-stu-id="41205-146"><dt>**Zero integer**</dt></span></span> </dl>                 | <span data-ttu-id="41205-147">傳回指定之索引鍵的字串類別名稱。</span><span class="sxs-lookup"><span data-stu-id="41205-147">Returns the string class name for the designated key.</span></span><br/>                                                                                        |
| <span id="Empty_string____"></span><span id="empty_string____"></span><span id="EMPTY_STRING____"></span><dl> <span data-ttu-id="41205-148"><dt>**空字串 ""**</dt></span><span class="sxs-lookup"><span data-stu-id="41205-148"><dt>**Empty string " "**</dt></span></span> </dl> | <span data-ttu-id="41205-149">傳回登錄機碼的預設值。</span><span class="sxs-lookup"><span data-stu-id="41205-149">Returns the default value of the registry key.</span></span><br/>                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41205-150">傳回值</span><span class="sxs-lookup"><span data-stu-id="41205-150">Return value</span></span>

<span data-ttu-id="41205-151">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="41205-151">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="41205-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="41205-152">Requirements</span></span>



| <span data-ttu-id="41205-153">需求</span><span class="sxs-lookup"><span data-stu-id="41205-153">Requirement</span></span> | <span data-ttu-id="41205-154">值</span><span class="sxs-lookup"><span data-stu-id="41205-154">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41205-155">版本</span><span class="sxs-lookup"><span data-stu-id="41205-155">Version</span></span><br/> | <span data-ttu-id="41205-156">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="41205-156">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="41205-157">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="41205-157">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="41205-158">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="41205-158">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="41205-159">DLL</span><span class="sxs-lookup"><span data-stu-id="41205-159">DLL</span></span><br/>     | <dl> <span data-ttu-id="41205-160"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41205-160"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="41205-161">IID</span><span class="sxs-lookup"><span data-stu-id="41205-161">IID</span></span><br/>     | <span data-ttu-id="41205-162">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="41205-162">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 
