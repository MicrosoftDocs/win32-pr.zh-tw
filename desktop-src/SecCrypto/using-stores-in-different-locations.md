---
description: 下列範例示範使用存放區物件的各個層面。 它會顯示 CAPICOM 記憶體存放區中的開啟存放區 \_ \_ 、capicom \_ 目前 \_ \_ 的使用者存放區，以及 capicom \_ 本機 \_ 電腦 \_ 存放區的位置。
ms.assetid: bfb7ff48-1d6b-404f-9dd4-6de1898354b7
title: 使用不同位置的商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e22fa4d4eca4748d6c4652a8b33d22a1db492a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691396"
---
# <a name="using-stores-in-different-locations"></a><span data-ttu-id="e75dd-104">使用不同位置的商店</span><span class="sxs-lookup"><span data-stu-id="e75dd-104">Using Stores in Different Locations</span></span>

<span data-ttu-id="e75dd-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="e75dd-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e75dd-106">相反地，請使用 .NET Framework 來執行安全性功能。</span><span class="sxs-lookup"><span data-stu-id="e75dd-106">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="e75dd-107">如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]</span><span class="sxs-lookup"><span data-stu-id="e75dd-107">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="e75dd-108">下列範例示範使用 [**存放區**](store.md) 物件的各個層面。</span><span class="sxs-lookup"><span data-stu-id="e75dd-108">The following example demonstrates aspects of working with the [**Store**](store.md) object.</span></span> <span data-ttu-id="e75dd-109">它會顯示 CAPICOM 記憶體存放區中的開啟存放區 \_ \_ 、capicom \_ 目前 \_ \_ 的使用者存放區，以及 capicom \_ 本機 \_ 電腦 \_ 存放區的位置。</span><span class="sxs-lookup"><span data-stu-id="e75dd-109">It shows opening stores in the CAPICOM\_MEMORY\_STORE, CAPICOM\_CURRENT\_USER\_STORE, and CAPICOM\_LOCAL\_MACHINE\_STORE locations.</span></span>

<span data-ttu-id="e75dd-110">此範例顯示從開啟的 [*存放區*](../secgloss/c-gly.md)匯出 [*憑證*](../secgloss/c-gly.md)、將匯出的憑證寫入檔案、將其讀取並匯入至不同的存放區。</span><span class="sxs-lookup"><span data-stu-id="e75dd-110">The example shows exporting [*certificates*](../secgloss/c-gly.md) from an open [*store*](../secgloss/c-gly.md), writing the exported certificates to a file, reading them back in and importing them into a different store.</span></span> <span data-ttu-id="e75dd-111">然後會列舉和顯示新匯入的憑證。</span><span class="sxs-lookup"><span data-stu-id="e75dd-111">The newly imported certificates are then enumerated and displayed.</span></span>

<span data-ttu-id="e75dd-112">在任何的 CAPICOM 錯誤中 **，會傳回** 負數值的負數值。</span><span class="sxs-lookup"><span data-stu-id="e75dd-112">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="e75dd-113">如需詳細資訊，請參閱 [**CAPICOM \_ 錯誤碼 \_**](capicom-error-code.md)。</span><span class="sxs-lookup"><span data-stu-id="e75dd-113">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="e75dd-114">如需有關 **錯誤** 之正十進位值的詳細資訊，請參閱 winerror.h。</span><span class="sxs-lookup"><span data-stu-id="e75dd-114">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


```VB
Sub OpenStores()

    On Error GoTo ErrorHandler

    'Open Memory, current user, and local machine stores
    Dim MemoryStore As New Store
    Dim CurrentUserStore As New Store
    Dim LocalMachineStore As New Store
    Dim NumCerts As Integer

    MemoryStore.Open(CAPICOM_MEMORY_STORE, "MemStore", _
        CAPICOM_STORE_OPEN_READ_WRITE)
    CurrentUserStore.Open(CAPICOM_CURRENT_USER_STORE, _
        CAPICOM_MY_STORE, CAPICOM_STORE_OPEN_READ_ONLY)
    LocalMachineStore.Open(CAPICOM_LOCAL_MACHINE_STORE, _
        CAPICOM_CA_STORE, CAPICOM_STORE_OPEN_READ_ONLY)

    ' Check the number of certificates in the stores.
    NumCerts = MemoryStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates in the memory store. ")
    NumCerts = CurrentUserStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates in the current user store. ")
    NumCerts = LocalMachineStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates in the local machine store. ")


    '  Export the certificates in the current user MY store
    '  to a file.
    Dim ExportString As String
    ExportString = CurrentUserStore.Export
Open "Exportcerts.txt" For Output As #1
Write #1, ExportString
Close #1

    ' Read the store the file.
    Dim importString As String
Open "exportcerts.txt" For Input As #2
Input #2, importString
Close #2
    MemoryStore.Import(importString)

    ' Check the number of certificates in the memory store after 
    ' import()
    NumCerts = MemoryStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates now in the memory store. ")

    ' Enumerate the certificates in the memory store and display each
    ' certificate
    Dim i As Long
    For i = 1 To NumCerts
        MemoryStore.Certificates.Item(i).Display()
    Next i

    ' Release the store objects
    MemoryStore = Nothing
    CurrentUserStore = Nothing
    LocalMachineStore = Nothing
    Exit Sub
ErrorHandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found: " & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 
