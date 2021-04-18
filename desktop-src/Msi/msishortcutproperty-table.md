---
description: MsiShortcutProperty 資料表可讓 Window Installer 設定也是 Windows Shell 物件的快捷方式屬性。
ms.assetid: d959769d-113f-4af2-89d4-ad3f5322de33
title: MsiShortcutProperty 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f295feabd6ff9b1677fdcf47791959b0fbb8a920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513860"
---
# <a name="msishortcutproperty-table"></a><span data-ttu-id="c65d2-103">MsiShortcutProperty 資料表</span><span class="sxs-lookup"><span data-stu-id="c65d2-103">MsiShortcutProperty Table</span></span>

<span data-ttu-id="c65d2-104">MsiShortcutProperty 資料表可讓 Window Installer 設定也是 [Windows Shell](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) 物件的快捷方式屬性。</span><span class="sxs-lookup"><span data-stu-id="c65d2-104">The MsiShortcutProperty table enables Window Installer to set properties for shortcuts that are also [Windows Shell](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) objects.</span></span> <span data-ttu-id="c65d2-105">從 Windows Vista 和 Windows Server 2008 開始，Windows Shell 會為 Shell 物件（例如快速鍵）提供 IPropertyStore 介面。</span><span class="sxs-lookup"><span data-stu-id="c65d2-105">Beginning with Windows Vista and Windows Server 2008 the Windows Shell provides an IPropertyStore Interface for shell objects such as shortcuts.</span></span> <span data-ttu-id="c65d2-106">安裝快捷方式時，在 Windows Server 2008 R2 或 Windows 7 上執行的 Windows Installer 5.0 套件可以設定這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c65d2-106">A Windows Installer 5.0 package running on Windows Server 2008 R2 or Windows 7 can set these properties when the shortcut is installed.</span></span>

<span data-ttu-id="c65d2-107">**[Windows Installer 4.5 或更早版本](not-supported-in-windows-installer-4-5.md)：** 不支援。</span><span class="sxs-lookup"><span data-stu-id="c65d2-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="c65d2-108">從 Windows Installer 5.0 開始，可以使用此資料表。</span><span class="sxs-lookup"><span data-stu-id="c65d2-108">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="c65d2-109">MsiShortcutProperty 資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="c65d2-109">The MsiShortcutProperty table has the following columns.</span></span>



| <span data-ttu-id="c65d2-110">Column</span><span class="sxs-lookup"><span data-stu-id="c65d2-110">Column</span></span>              | <span data-ttu-id="c65d2-111">類型</span><span class="sxs-lookup"><span data-stu-id="c65d2-111">Type</span></span>                         | <span data-ttu-id="c65d2-112">答案</span><span class="sxs-lookup"><span data-stu-id="c65d2-112">Key</span></span> | <span data-ttu-id="c65d2-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="c65d2-113">Nullable</span></span> |
|---------------------|------------------------------|-----|----------|
| <span data-ttu-id="c65d2-114">MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="c65d2-114">MsiShortcutProperty</span></span> | [<span data-ttu-id="c65d2-115">識別碼</span><span class="sxs-lookup"><span data-stu-id="c65d2-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="c65d2-116">Y</span><span class="sxs-lookup"><span data-stu-id="c65d2-116">Y</span></span>   | <span data-ttu-id="c65d2-117">N</span><span class="sxs-lookup"><span data-stu-id="c65d2-117">N</span></span>        |
| <span data-ttu-id="c65d2-118">快速鍵\_</span><span class="sxs-lookup"><span data-stu-id="c65d2-118">Shortcut\_</span></span>          | [<span data-ttu-id="c65d2-119">識別碼</span><span class="sxs-lookup"><span data-stu-id="c65d2-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="c65d2-120">N</span><span class="sxs-lookup"><span data-stu-id="c65d2-120">N</span></span>   | <span data-ttu-id="c65d2-121">N</span><span class="sxs-lookup"><span data-stu-id="c65d2-121">N</span></span>        |
| <span data-ttu-id="c65d2-122">PropertyKey</span><span class="sxs-lookup"><span data-stu-id="c65d2-122">PropertyKey</span></span>         | [<span data-ttu-id="c65d2-123">格式 化</span><span class="sxs-lookup"><span data-stu-id="c65d2-123">Formatted</span></span>](formatted.md)   | <span data-ttu-id="c65d2-124">N</span><span class="sxs-lookup"><span data-stu-id="c65d2-124">N</span></span>   | <span data-ttu-id="c65d2-125">N</span><span class="sxs-lookup"><span data-stu-id="c65d2-125">N</span></span>        |
| <span data-ttu-id="c65d2-126">PropVariantValue</span><span class="sxs-lookup"><span data-stu-id="c65d2-126">PropVariantValue</span></span>    | [<span data-ttu-id="c65d2-127">格式 化</span><span class="sxs-lookup"><span data-stu-id="c65d2-127">Formatted</span></span>](formatted.md)   | <span data-ttu-id="c65d2-128">N</span><span class="sxs-lookup"><span data-stu-id="c65d2-128">N</span></span>   | <span data-ttu-id="c65d2-129">N</span><span class="sxs-lookup"><span data-stu-id="c65d2-129">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="c65d2-130">資料行</span><span class="sxs-lookup"><span data-stu-id="c65d2-130">Columns</span></span>

<dl> <dt>

<span data-ttu-id="c65d2-131"><span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>MsiShortcutProperty</span><span class="sxs-lookup"><span data-stu-id="c65d2-131"><span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>MsiShortcutProperty</span></span>
</dt> <dd>

<span data-ttu-id="c65d2-132">MsiShortcutProperty 資料表中這個資料列的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="c65d2-132">Unique identifier for this row of the MsiShortcutProperty table.</span></span>

</dd> <dt>

<span data-ttu-id="c65d2-133"><span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>快捷方式\_</span><span class="sxs-lookup"><span data-stu-id="c65d2-133"><span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Shortcut\_</span></span>
</dt> <dd>

<span data-ttu-id="c65d2-134">[快速鍵](shortcut-table.md)資料表中的索引鍵，識別具有屬性集的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="c65d2-134">A key into the [Shortcut](shortcut-table.md) table that identifies the shortcut having a property set.</span></span>

</dd> <dt>

<span data-ttu-id="c65d2-135"><span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey</span><span class="sxs-lookup"><span data-stu-id="c65d2-135"><span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey</span></span>
</dt> <dd>

<span data-ttu-id="c65d2-136">提供 [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) 結構資訊的字串值。</span><span class="sxs-lookup"><span data-stu-id="c65d2-136">A string value that provides information for the [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structure.</span></span> <span data-ttu-id="c65d2-137">此欄位中的資訊必須參考以 Windows 屬性系統註冊之屬性的標準名稱。</span><span class="sxs-lookup"><span data-stu-id="c65d2-137">The information in this field must refer to the canonical name of a property registered with the Windows property system.</span></span> <span data-ttu-id="c65d2-138">如需 Windows 屬性系統的詳細資訊，請參閱 [屬性系統總覽](/previous-versions//bb776909(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="c65d2-138">For more information about the Windows property system, see the [Property System Overview](/previous-versions//bb776909(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="c65d2-139"><span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue</span><span class="sxs-lookup"><span data-stu-id="c65d2-139"><span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue</span></span>
</dt> <dd>

<span data-ttu-id="c65d2-140">提供 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構資訊的字串值。</span><span class="sxs-lookup"><span data-stu-id="c65d2-140">A string value that provides information for the [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure.</span></span>

</dd> </dl>

<span data-ttu-id="c65d2-141">在快捷方式上可以設定多個屬性。</span><span class="sxs-lookup"><span data-stu-id="c65d2-141">Multiple properties can be set on a shortcut.</span></span> <span data-ttu-id="c65d2-142">如果相同的快捷方式上已多次設定相同的屬性，則會以未指定的順序來設定值。</span><span class="sxs-lookup"><span data-stu-id="c65d2-142">If the same property is set multiple times on the same shortcut the value is set in an unspecified order.</span></span>

<span data-ttu-id="c65d2-143">Windows Installer 只有在已安裝或重新安裝快捷方式時，才能設定快速鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="c65d2-143">Windows Installer can set shortcut properties only when the shortcut is installed or reinstalled.</span></span> <span data-ttu-id="c65d2-144">未重新安裝已安裝之快捷方式的修補程式不會更新快捷方式的屬性。</span><span class="sxs-lookup"><span data-stu-id="c65d2-144">A patch that does not reinstall a shortcut that has already been installed does not update the shortcut's properties.</span></span> <span data-ttu-id="c65d2-145">Patch 可以藉由在修補程式套件中加入 [快捷方式](shortcut-table.md) 表，並重新安裝快捷方式來更新屬性。</span><span class="sxs-lookup"><span data-stu-id="c65d2-145">A patch can update the properties by including a [Shortcut](shortcut-table.md) table in the patch package and reinstalling the shortcut.</span></span>

## <a name="remarks"></a><span data-ttu-id="c65d2-146">備註</span><span class="sxs-lookup"><span data-stu-id="c65d2-146">Remarks</span></span>

<span data-ttu-id="c65d2-147">[Windows Installer 錯誤訊息](windows-installer-error-messages.md) 1946 會以警告傳回，而且如果 Windows Installer 無法設定 MsiShortcutProperty 資料表中指定的快捷方式屬性，則會繼續安裝。</span><span class="sxs-lookup"><span data-stu-id="c65d2-147">[Windows Installer Error Message](windows-installer-error-messages.md) 1946 is returned as a warning, and the installation continues, if Windows Installer is unable to set a shortcut property specified in the MsiShortcutProperty table.</span></span>

## <a name="validation"></a><span data-ttu-id="c65d2-148">驗證</span><span class="sxs-lookup"><span data-stu-id="c65d2-148">Validation</span></span>

<dl>

[<span data-ttu-id="c65d2-149">ICE03</span><span class="sxs-lookup"><span data-stu-id="c65d2-149">ICE03</span></span>](ice03.md)  
</dl>

 

 
