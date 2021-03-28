---
description: 從專案的屬性集取得屬性的值。 屬性可以依照名稱或屬性集的格式識別碼來指定 (FMTID) 和屬性識別碼 (PID) 。
ms.assetid: ca787d7b-d95a-45b9-9627-fd505f99f868
title: 'ShellFolderItem. ExtendedProperty 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.ExtendedProperty
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 614e42512b17a0d8a6950ac96914128b8746c685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973592"
---
# <a name="shellfolderitemextendedproperty-method"></a><span data-ttu-id="99bfc-104">ShellFolderItem. ExtendedProperty 方法</span><span class="sxs-lookup"><span data-stu-id="99bfc-104">ShellFolderItem.ExtendedProperty method</span></span>

<span data-ttu-id="99bfc-105">從專案的屬性集取得屬性的值。</span><span class="sxs-lookup"><span data-stu-id="99bfc-105">Gets the value of a property from an item's property set.</span></span> <span data-ttu-id="99bfc-106">屬性可以依照名稱或屬性集的格式識別碼來指定 (FMTID) 和屬性識別碼 (PID) 。</span><span class="sxs-lookup"><span data-stu-id="99bfc-106">The property can be specified either by name or by the property set's format identifier (FMTID) and property identifier (PID).</span></span>

## <a name="syntax"></a><span data-ttu-id="99bfc-107">語法</span><span class="sxs-lookup"><span data-stu-id="99bfc-107">Syntax</span></span>


```JScript
retVal = ShellFolderItem.ExtendedProperty(
  sPropName
)
```



## <a name="parameters"></a><span data-ttu-id="99bfc-108">參數</span><span class="sxs-lookup"><span data-stu-id="99bfc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99bfc-109">*sPropName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="99bfc-109">*sPropName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99bfc-110">類型： **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="99bfc-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="99bfc-111">指定屬性的 **字串** 值。</span><span class="sxs-lookup"><span data-stu-id="99bfc-111">A **String** value that specifies the property.</span></span> <span data-ttu-id="99bfc-112">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="99bfc-112">See the Remarks section for details.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99bfc-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="99bfc-113">Return value</span></span>

<span data-ttu-id="99bfc-114">類型： \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="99bfc-114">Type: \**Variant\** _</span></span>

<span data-ttu-id="99bfc-115">當此方法傳回時，會包含屬性的值（如果它存在於指定的專案中）。</span><span class="sxs-lookup"><span data-stu-id="99bfc-115">When this method returns, contains the value of the property, if it exists for the specified item.</span></span> <span data-ttu-id="99bfc-116">此值將會有完整的輸入，例如，日期會以日期（而不是字串）的形式傳回。</span><span class="sxs-lookup"><span data-stu-id="99bfc-116">The value will have full typing—for example, dates are returned as dates, not strings.</span></span>

<span data-ttu-id="99bfc-117">如果屬性有效但不存在於指定的專案，則這個方法會傳回長度為零的字串，否則會傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="99bfc-117">This method returns a zero-length string if the property is valid but does not exist for the specified item, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="99bfc-118">備註</span><span class="sxs-lookup"><span data-stu-id="99bfc-118">Remarks</span></span>

<span data-ttu-id="99bfc-119">有兩種方式可以指定屬性。</span><span class="sxs-lookup"><span data-stu-id="99bfc-119">There are two ways to specify a property.</span></span> <span data-ttu-id="99bfc-120">第一個是指派屬性的已知名稱，例如 "Author" 或 "Date"，以 _sPropName \*。</span><span class="sxs-lookup"><span data-stu-id="99bfc-120">The first is to assign the property's well-known name, such as "Author" or "Date", to _sPropName\*.</span></span> <span data-ttu-id="99bfc-121">不過，每個屬性都是元件物件模型 (COM) 屬性集的成員，也可以藉由指定其格式識別碼 (FMTID) 和屬性識別碼 (PID) 來識別。</span><span class="sxs-lookup"><span data-stu-id="99bfc-121">However, each property is a member of a Component Object Model (COM) property set and can also be identified by specifying its format ID (FMTID) and property ID (PID).</span></span> <span data-ttu-id="99bfc-122">[**FMTID**](../stg/structured-storage-serialized-property-set-format.md)是識別屬性集的 GUID，而 [**PID**](../stg/structured-storage-serialized-property-set-format.md)是識別屬性集內特定屬性的整數。</span><span class="sxs-lookup"><span data-stu-id="99bfc-122">An [**FMTID**](../stg/structured-storage-serialized-property-set-format.md) is a GUID that identifies the property set, and a [**PID**](../stg/structured-storage-serialized-property-set-format.md) is an integer that identifies a particular property within the property set.</span></span>

<span data-ttu-id="99bfc-123">依 FMTID/PID 值指定屬性，通常比使用其名稱更有效率。</span><span class="sxs-lookup"><span data-stu-id="99bfc-123">Specifying a property by its FMTID/PID values is usually more efficient than using its name.</span></span> <span data-ttu-id="99bfc-124">若要使用屬性的 FMTID/PID 值搭配 **ExtendedProperty**，必須將它們合併成 SCID。</span><span class="sxs-lookup"><span data-stu-id="99bfc-124">To use a property's FMTID/PID values with **ExtendedProperty**, they must be combined into an SCID.</span></span> <span data-ttu-id="99bfc-125">SCID 是包含 FMTID/PID 值的字串，其格式為 "*FMTID \* \* pid*"，其中 FMTID 是屬性集 GUID 的字串形式。</span><span class="sxs-lookup"><span data-stu-id="99bfc-125">An SCID is a string that contains the FMTID/PID values in the form "*FMTID\*\*PID*", where the FMTID is the string form of the property set's GUID.</span></span> <span data-ttu-id="99bfc-126">例如，摘要資訊屬性集的作者屬性的 SCID 是 "{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4"。</span><span class="sxs-lookup"><span data-stu-id="99bfc-126">For example, the SCID of the summary information property set's author property is "{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4".</span></span>

<span data-ttu-id="99bfc-127">如需 Shell 目前支援的 FMTIDs 和 Pid 清單，請參閱 [**SHCOLUMNID**](./objects.md)。</span><span class="sxs-lookup"><span data-stu-id="99bfc-127">For a list of FMTIDs and PIDs that are currently supported by the Shell, see [**SHCOLUMNID**](./objects.md).</span></span>

## <a name="examples"></a><span data-ttu-id="99bfc-128">範例</span><span class="sxs-lookup"><span data-stu-id="99bfc-128">Examples</span></span>

<span data-ttu-id="99bfc-129">此範例程式碼說明如何使用 **ExtendedProperty** 從 Word 檔取出 "Title" 和 "Author" 屬性。</span><span class="sxs-lookup"><span data-stu-id="99bfc-129">This sample code illustrates how to use **ExtendedProperty** to retrieve the "Title" and "Author" properties from a Word document.</span></span> <span data-ttu-id="99bfc-130">一旦您有與檔案相關聯的 [**ShellFolderItem**](shellfolderitem-object.md) 物件，在此範例中， *fiWordDoc* 將其名稱傳遞給 **ExtendedProperty**，以抓取屬性的值。</span><span class="sxs-lookup"><span data-stu-id="99bfc-130">Once you have the [**ShellFolderItem**](shellfolderitem-object.md) object associated with the file, *fiWordDoc* in this example, retrieve the property's value by passing its name to **ExtendedProperty**.</span></span>


```none
...
Doc_Title=fiWordDoc.ExtendedProperty("DocTitle")
Doc_Author=fiWordDoc.ExtendedProperty("Author")
...
```



<span data-ttu-id="99bfc-131">更快速且更有效率的方法是將 SCID 傳遞至 **ExtendedProperty**。</span><span class="sxs-lookup"><span data-stu-id="99bfc-131">A faster and more efficient approach is to pass an SCID to **ExtendedProperty**.</span></span>


```none
...
FMTID_SummaryInfo="{F29F85E0-4FF9-1068-AB91-08002B27B3D9}"
PID_TITLE="2"
PID_AUTHOR="4"
SCID_TITLE=FMTID_SummaryInfo+" "+PID_TITLE
SCID_AUTHOR=FMTID_SummaryInfo+" "+PID_AUTHOR
Doc_Title=fiWordDoc.ExtendedProperty(SCID_TITLE)
Doc_Author=fiWordDoc.ExtendedProperty(SCID_AUTHOR)
...
```



<span data-ttu-id="99bfc-132">下列範例會針對 JScript、VBScript 和 Visual Basic 示範此方法的適當用法。</span><span class="sxs-lookup"><span data-stu-id="99bfc-132">The following examples show the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="99bfc-133">Jscript：</span><span class="sxs-lookup"><span data-stu-id="99bfc-133">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItem2ExtendedPropertyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                var szReturn = "";
                
                szReturn = objFolderItem.ExtendedProperty("infotip");
                alert(szReturn);
            }
        }
    }
</script>
```



<span data-ttu-id="99bfc-134">VBScript</span><span class="sxs-lookup"><span data-stu-id="99bfc-134">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemExtendedPropertyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    dim szReturn
                    
                    szReturn = objFolderItem.ExtendedProperty("type")
                    alert(szReturn)
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="99bfc-135">Visual Basic：</span><span class="sxs-lookup"><span data-stu-id="99bfc-135">Visual Basic:</span></span>


```VB
Private Sub fnFolderItem2ExtendedPropertyVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem2.ExtendedProperty("size")
                    Debug.Print szReturn
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="99bfc-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="99bfc-136">Requirements</span></span>



| <span data-ttu-id="99bfc-137">需求</span><span class="sxs-lookup"><span data-stu-id="99bfc-137">Requirement</span></span> | <span data-ttu-id="99bfc-138">值</span><span class="sxs-lookup"><span data-stu-id="99bfc-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="99bfc-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99bfc-139">Minimum supported client</span></span><br/> | <span data-ttu-id="99bfc-140">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99bfc-140">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="99bfc-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99bfc-141">Minimum supported server</span></span><br/> | <span data-ttu-id="99bfc-142">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99bfc-142">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="99bfc-143">標頭</span><span class="sxs-lookup"><span data-stu-id="99bfc-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="99bfc-144"><dt>Shldisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="99bfc-144"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="99bfc-145">Idl</span><span class="sxs-lookup"><span data-stu-id="99bfc-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="99bfc-146"><dt>Shldisp .idl</dt></span><span class="sxs-lookup"><span data-stu-id="99bfc-146"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="99bfc-147">DLL</span><span class="sxs-lookup"><span data-stu-id="99bfc-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99bfc-148"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="99bfc-148"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
