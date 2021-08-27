---
title: 在顯示規範中註冊內容功能表 COM 物件
description: 本主題說明需要修改才能註冊內容功能表 COM 物件的登錄機碼。
ms.assetid: 389bc249-4849-4763-9d1b-b35598a51050
ms.tgt_platform: multiple
keywords:
- 在顯示規範中註冊內容功能表 COM 物件
- 內容功能表 COM 物件廣告，註冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5650d5864093293728e5c4f1157980c76bffa0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881242"
---
# <a name="registering-the-context-menu-com-object-in-a-display-specifier"></a>在顯示規範中註冊內容功能表 COM 物件

當您使用 COM 建立 Active Directory 目錄服務的內容功能表延伸 DLL 時，必須向 Windows 登錄註冊擴充功能，並 Active Directory Domain Services 以通知 Active Directory 系統管理 MMC 嵌入式管理單元和延伸模組的 Windows shell。

## <a name="registering-in-the-windows-registry"></a>在 Windows 登錄中註冊

和所有 COM 伺服器一樣，必須在登錄中註冊內容功能表延伸。 此擴充功能會在下列機碼下註冊。

```
HKEY_CLASSES_ROOT
   CLSID
      <clsid>
```

*&lt; Clsid &gt;* 是 [**STRINGFROMCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid)函數所產生之 clsid 的字串表示。 在 *&lt; &gt; clsid* 機碼下，有一個 **InProcServer32** 機碼會將物件識別為32位的內部進程伺服器。 在 **InProcServer32** 索引鍵下，DLL 的位置會指定為預設值，而執行緒模型則是在 **>threadingmodel** 值中指定。 所有內容功能表延伸都必須使用「單元」執行緒模型。

## <a name="registering-with-active-directory-domain-services"></a>向 Active Directory Domain Services 註冊

操作功能表延伸模組註冊是特定于一個地區設定。 如果內容功能表延伸模組套用至所有地區設定，則必須在 [顯示規範] 容器中所有地區設定子容器的物件類別 [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) 物件中註冊。 如果內容功能表延伸針對特定地區設定進行當地語系化，則必須在該地區設定的 subcontainer 中，將它註冊在 **displaySpecifier** 物件中。 如需顯示規範容器和地區設定的詳細資訊，請參閱 [顯示](display-specifiers.md) 規範和 [DisplaySpecifiers 容器](displayspecifiers-container.md)。

有兩個顯示規範屬性可以在其中註冊內容功能表延伸模組專案。 這些都是 [**adminCoNtextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) 和 [**shellCoNtextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu)。

[**AdminCoNtextMenu**](/windows/desktop/ADSchema/a-admincontextmenu)屬性會識別要在 Active Directory 系統管理嵌入式管理單元中顯示的系統管理內容功能表。當使用者在其中一個 Active Directory 系統管理 MMC 嵌入式管理單元中顯示適當類別的物件內容功能表時，就會顯示內容功能表。

[**shellCoNtextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu)屬性會識別要在 Windows shell 中顯示的使用者內容功能表。 當使用者在 Windows 檔案總管中，流覽適當類別的物件內容功能表時，就會顯示內容功能表。 從 Windows Server 2003 開始，Windows shell 不會再顯示 Active Directory Domain Services 的物件。

所有這些屬性都是多重值。

註冊內容功能表延伸模組時， [**adminCoNtextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) 和 [**shellCoNtextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) 屬性的值需要下列格式。


```C++
<order number>,<clsid>
```



「 &lt; 訂單編號」 &gt; 是一個不帶正負號的數位，代表內容功能表中的專案位置。 顯示內容功能表時，會使用每個值的「訂單編號」比較來排序這些值 &lt; &gt; 。 如果有一個以上的值具有相同的「 &lt; 訂單編號」 &gt; ，則這些內容功能表延伸模組會以從 Active Directory 伺服器讀取的順序載入。 可能的話，請使用非現有的「 &lt; 訂單編號」 &gt; ，也就是屬性中其他值尚未使用的「訂單編號」。 「訂單編號」序列中不允許有指定的開始位置和間距 &lt; &gt; 。

" &lt; Clsid &gt; " 是 [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) 函式所產生之 clsid 的字串表示。

在 Windows shell 中，支援多重選取的內容功能表項目。 在此情況下，會針對每個選取的物件叫用內容功能表延伸。 在 Active Directory 系統管理嵌入式管理單元中，也支援多重選取的內容功能表擴充功能專案。 在此情況下， [**DSOBJECTNAMES**](/windows/desktop/api/Dsclient/ns-dsclient-dsobjectnames) 結構將會包含所選取的每個目錄物件的 [**DSOBJECT**](/windows/desktop/api/Dsclient/ns-dsclient-dsobject) 結構。

> [!IMPORTANT]
> 針對 Windows shell，會在使用者登入時抓取顯示規範資訊，並針對使用者的會話進行快取。 針對系統管理嵌入式管理單元，在載入嵌入式管理單元時，會抓取顯示規範資料，而且會在進程期間進行快取。 針對 Windows shell，這表示在使用者登出後重新登入後，顯示規範的變更會生效。 系統管理嵌入式管理單元的變更會在嵌入式管理單元或主控台檔案重載時生效，也就是當您啟動新的主控台檔案實例或新的 Mmc.exe 實例並新增嵌入式管理單元時，會抓取最新的顯示規範資料。

 

如需詳細資訊，以及如何執行內容功能表延伸模組的程式碼範例，請參閱 [執行內容功能表 COM 物件的範例程式碼](example-code-for-implementation-of-the-context-menu-com-object.md)。

 

 
