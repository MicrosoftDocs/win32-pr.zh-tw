---
description: 有時候，您可能只想要更新一部分的實例。
ms.assetid: c92bf8f9-9cac-4cf0-a45d-f60aee5a9ec2
ms.tgt_platform: multiple
title: 更新部分實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eaf58bfc151358a2b4f282815769d1b19c068f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971714"
---
# <a name="updating-part-of-an-instance"></a>更新部分實例

有時候，您可能只想要更新一部分的實例。 例如，某些實例有大量的屬性。 如果您必須更新大量的實例，可能會降低系統效能。 因此，您可以選擇只更新部分的實例，進而減少您必須在 WMI 中傳送和取出的資訊量。 不過，WMI 不直接支援部分實例作業，也不會執行大部分的提供者。 因此，如果您撰寫的應用程式會使用部分實例作業，請使用 **wbem \_ e \_ 提供者 \_ 無法 \_** 使用或 **\_ \_ 不 \_ 支援** 在 c + + 中使用 wbem e 的錯誤碼，來準備您的呼叫失敗。 在指令碼語言中，錯誤碼可能是 **wbemErrProviderNotCapable** 或 **wbemErrNotSupported**。

在腳本中，這項作業只有在透過企業更新極大量物件中的一或兩個可寫入屬性時，才需要協助效能。 否則，一般 VBScript 會呼叫 [**SWbemObject. Put \_**](swbemobject-put-.md)或 [**SWbemObject PutAsync \_**](swbemobject-putasync-.md)，而如同寫入整個物件時，實際上只會更新提供者已啟用寫入的屬性。

下列程式描述如何使用 PowerShell 要求部分實例更新。

**使用 PowerShell 要求部分實例更新**

1.  取得您想要更新之物件的路徑。

    您可以手動描述路徑，或查詢物件，然後取得 **\_ \_ path** 屬性。

    ```PowerShell
    $myWMIDrivePath = (get-wmiObject Win32_LogicalDisk -filter "Name = 'C:'").__Path
    #or
    $myWmiDrivePath = \\myComputer\root\cimv2:Win32_LogicalDisk.DeviceID="C:"
    ```

    

2.  設定雜湊表，其中列出要更新的屬性名稱，並在 [set-wmiinstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true)的呼叫中使用此雜湊表。

    ```PowerShell
    $newDriveName = @{VolumeName = "OSDisk"}
    Set-WmiInstance -Path $myWMIDrivePath -Arguments $newDriveName
    ```

    

下列程式說明如何使用 c # 要求部分實例更新。

> [!Note]  
> **系統管理** 是用來存取 WMI 的原始 .net 命名空間;不過，這個命名空間中的 Api 通常會較慢，而且也不會相對於其較新式的 **Microsoft 管理元件** 對應專案。

 

**使用 C 要求部分實例更新#**

1.  建立新的 [system.management.managementobject](/dotnet/api/system.management.managementobject) 物件，代表要更新的特定實例。

    ```PowerShell
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

2.  使用 [system.management.managementobject. SetPropertyValue](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_)的呼叫來設定屬性值。

    ```CSharp
    myDisk.SetPropertyValue("VolumeName", "OSDisk");
    ```

    

下列程式描述如何使用 VBScript 要求部分實例更新。

**使用 VBScript 要求部分實例更新**

1.  建立 [**SWbemNamedValueSet**](swbemnamedvalueset.md) 內容物件。

    ```VB
    Set objwbemNamedValueSet = CreateObject ("WbemScripting.SWbemNamedValueSet")
    ```

    

2.  使用 SWbemNamedValueSet. Add 方法，將 Put 延伸模組值「 \_ \_ put \_ 延伸」和「 \_ \_ put \_ EXT CLIENT 要求」新增 \_ \_ 至內容物件。 [](swbemnamedvalueset-add.md)

    ```VB
    objwbemNamedValueSet.Add "__PUT_EXTENSIONS", True
    objwbemNamedValueSet.Add "__PUT_EXT_CLIENT_REQUEST", True
    ```

    

3.  設定陣列，其中列出要更新的屬性名稱，並將此陣列新增至副檔名值[](swbemnamedvalueset.md)為 " \_ \_ put \_ EXT \_ properties" 的 SWbemNamedValueSet 內容物件。

    ```VB
    arProperties = Array("propertyname1", "propertyname2") 
    objwbemNamedValueSet.Add "__PUT_EXT_PROPERTIES", arProperties
    ```

    

4.  將 SWbemObject 的 *iFlags* 參數設定為 **wbemChangeFlagUpdateOnly** 的 [**Put \_**](swbemobject-put-.md)呼叫。 若未使用此旗標，則呼叫會失敗，並出現不正確內容。

5.  在 [**SWbemObject. Put \_**](swbemobject-put-.md)或 [**SWbemObject. PutAsync \_**](swbemobject-putasync-.md)的 *objwbemNamedValueSet* 參數中，將您的旗標和內容物件傳遞給提供者。

    ```VB
    call objSystem.put_( wbemChangeFlagUpdateOnly, objwbemNamedValueSet)
    ```

    

下列程式描述如何使用 c + + 要求部分實例更新。

**使用 c + + 要求部分實例更新**

1.  使用對 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)的呼叫來建立 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)物件。

    內容物件是 WMI 用來將更多資訊傳遞給 WMI 提供者的物件。 在此情況下，您會使用 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) 物件來指示提供者接受部分實例更新。

2.  \_ \_ \_ 使用 IWbemCoNtext：： SetValue 的呼叫，將「put 延伸」和「 \_ \_ put \_ EXT \_ CLIENT \_ 要求」命名值新增 [](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue)至 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)物件。

    下表列出「put 延伸模組」 \_ \_ \_ 和「 \_ \_ put \_ EXT \_ CLIENT \_ 要求」的意義。

    

    | 命名值                     | Description                                                                                                                                                                                                                                             |
    |---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | " \_ \_ PUT \_ EXTENSIONS"           | **VT \_BOOL** 設定為 **VARIANT \_ TRUE**。 值，指出已指定一個或多個其他內容值。 這可讓您快速檢查提供者內的內容物件，以判斷是否正在使用部分實例更新。 |
    | 「 \_ \_ 放置 \_ EXT \_ 用戶端 \_ 要求」 | **VT \_BOOL** 設定為 **VARIANT \_ TRUE**。 在初始要求期間由用戶端設定。 此值可用來防止重新進入錯誤。                                                                                                                   |

    

     

3.  \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 使用 [**IWbemCoNtext：： SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue)的另一個呼叫，在 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)物件中加入 put ext STRICT null、put ext 屬性，或將 ext 不可部分完成的任何組合。

    下表列出已命名值的意義。

    

    | 命名值                   | Description                                                                                                                                                                                                                                   |
    |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | " \_ \_ PUT \_ EXT \_ STRICT \_ Null" | **VT \_BOOL** 設定為 **VARIANT \_ TRUE**。 指出用戶端已刻意將屬性設為 **VT \_ Null** ，並預期寫入作業成功。 如果提供者無法將值設定為 **Null**，則應該回報錯誤。 |
    | " \_ \_ PUT \_ EXT \_ PROPERTIES"    | 字串的 [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) ，包含要更新之屬性名稱的清單。 可以單獨使用，或搭配「 \_ \_ PUT \_ EXT 屬性」一起使用 \_ 。 這些值位於所寫入的實例中。                           |
    | " \_ \_ PUT EXT 不可部分完成 \_ \_ "        | **VT \_BOOL** 設定為 **VARIANT \_ TRUE**。 指出所有更新都必須同時成功 (不可部分完成的語義) 或提供者必須還原。 可能沒有部分成功。 可以單獨使用，也可以與其他旗標搭配使用。     |

    

     

4.  將 *iFlags* 參數設定為 **[ \_ \_ \_ 僅限 WBEM 旗標更新**]。 若未使用此旗標，則呼叫會失敗，並出現不正確內容。
5.  將 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)內容物件傳遞至 *pCtx* 參數中的任何 [**IWbemServices：:P Utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)或 [**iwbemservices：:P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)的呼叫。

    傳遞 [**IWbemCoNtext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) 物件會指示提供者允許部分實例更新。 在完整實例的更新中，您會將 *pCtx* 設定為 **Null**。

    如果出現在呼叫中的內容物件不包含「PUT 延伸模組」，則提供者可能會寫入任何必要的屬性 \_ \_ \_ 。 如果 \_ \_ \_ 內容物件中有「PUT 延伸模組」，WMI 就會要求提供者必須遵守作業的語法，否則也會導致呼叫失敗。 如需詳細資訊，請參閱 [處理提供者中的拒絕存取訊息](impersonating-a-client.md)。

 

 
