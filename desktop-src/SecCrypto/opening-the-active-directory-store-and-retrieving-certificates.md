---
description: 您可以從儲存網域使用者憑證的 Active Directory 存放區中取出憑證。
ms.assetid: 5c4d1629-88f3-41f4-afb3-7791cd590e6c
title: 開啟 Active Directory 儲存和正在抓取憑證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd60c7414aaec8b069817b47fbd2493bb11d98c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979942"
---
# <a name="opening-the-active-directory-store-and-retrieving-certificates"></a><span data-ttu-id="07966-103">開啟 Active Directory 儲存和正在抓取憑證</span><span class="sxs-lookup"><span data-stu-id="07966-103">Opening the Active Directory Store and Retrieving Certificates</span></span>

<span data-ttu-id="07966-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="07966-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="07966-105">相反地，請使用 .NET Framework 來執行安全性功能。</span><span class="sxs-lookup"><span data-stu-id="07966-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="07966-106">如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]</span><span class="sxs-lookup"><span data-stu-id="07966-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="07966-107">您可以從儲存網域使用者憑證的 Active Directory 存放區中取出 [*憑證*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="07966-107">[*Certificates*](../secgloss/c-gly.md) can be retrieved from an Active Directory store where the certificates of users of a domain are stored.</span></span> <span data-ttu-id="07966-108">Active Directory 存放區只能在唯讀模式中開啟，而且應用程式無法使用 CAPICOM 將憑證新增至 Active Directory 存放區或從中移除憑證。</span><span class="sxs-lookup"><span data-stu-id="07966-108">An Active Directory store can only be opened in the read-only mode and applications cannot added certificates to or remove certificates from an Active Directory store using CAPICOM.</span></span>

<span data-ttu-id="07966-109">在任何的 CAPICOM 錯誤中 **，會傳回** 負數值的負數值。</span><span class="sxs-lookup"><span data-stu-id="07966-109">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="07966-110">如需詳細資訊，請參閱 [**CAPICOM \_ 錯誤碼 \_**](capicom-error-code.md)。</span><span class="sxs-lookup"><span data-stu-id="07966-110">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="07966-111">如需有關 **錯誤** 之正十進位值的詳細資訊，請參閱 winerror.h。</span><span class="sxs-lookup"><span data-stu-id="07966-111">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="07966-112">下列範例示範如何開啟 Active Directory 存放區，以及從該存放區中取出憑證。</span><span class="sxs-lookup"><span data-stu-id="07966-112">The following example shows opening an Active Directory store and retrieving certificates from that store.</span></span>


```VB
Sub OpenADStore()
        On Error GoTo ErrorHandler
        Dim mystore As Store
        Set mystore = New Store
        
        ' Put a string that represents the name of a certificate 
        ' subject in SubjectNameCn. In the following example, 
        ' the * wildcard character is used in the string so that
        ' the Active Directory store will be searched for all 
        ' certificates with a subject name beginning with 'S.'
       
        Dim SubjectNameCn As String
        ' The following uses 'cn=' and the * wildcard character.
        ' Using this string, all certificates in the Active Directory
        ' store with a subject name beginning with an 'S' would
        ' be returned.

        SubjectNameCn = "CN=S*"
        
        ' Active Directory stores can only be opened with read-only
        ' access.
        
         mystore.Open CAPICOM_ACTIVE_DIRECTORY_USER_STORE, _
              SubjectNameCn, CAPICOM_STORE_OPEN_READ_ONLY
        
        If mystore.Certificates.Count < 1 Then
               MsgBox "A certificate for " & SubjectNameCn & _
                      " was not found "
        Else
               MsgBox "The certificate has been retrieved."
        End If
        
        Set mystore = Nothing
        Exit Sub

ErrorHandler:
         
         If Err.Number > 0 Then
               MsgBox "Visual Basic error found:" & Err.Description
         Else
               MsgBox "CAPICOM error found : " & Err.Number
         End If
End Sub
```



 

 
