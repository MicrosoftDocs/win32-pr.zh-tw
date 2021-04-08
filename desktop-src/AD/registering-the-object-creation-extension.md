---
title: 註冊物件建立延伸模組
description: 建立 Active Directory Domain Services 中的物件建立延伸模組 DLL 時，必須向 Windows 登錄註冊，並 Active Directory Domain Services，讓 COM 和 Active Directory 的系統管理 MMC 嵌入式管理單元知道此延伸模組。
ms.assetid: 6e950c6c-1a4f-4de0-9be1-004c31d4734c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27d8e2a50c2340d678fd43e546d68525afbc8a7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933048"
---
# <a name="registering-the-object-creation-extension"></a>註冊物件建立延伸模組

建立 Active Directory Domain Services 中的物件建立延伸模組 DLL 時，必須向 Windows 登錄註冊，並 Active Directory Domain Services，讓 COM 和 Active Directory 的系統管理 MMC 嵌入式管理單元知道此延伸模組。

## <a name="registering-in-the-windows-registry"></a>在 Windows 登錄中註冊

和所有 COM 伺服器一樣，必須在 Windows 登錄中註冊物件建立延伸模組。 此擴充功能會在下列機碼下註冊：

```
HKEY_CLASSES_ROOT
   CLSID
      <extension CLSID>
         InProcServer32
            (Default) = <extension path>
            ThreadingModel = Apartment
```

" &lt; EXTENSION CLSID &gt; " 是 [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) 函式所產生之 CLSID 的字串表示。 「 &lt; 擴充路徑」 &gt; 包含擴充 DLL 的路徑和檔案名。 所有物件建立延伸模組的 **>threadingmodel** 值都必須是 "公寓"。

## <a name="registering-with-active-directory-domain-services"></a>向 Active Directory Domain Services 註冊

物件建立延伸模組註冊是一種地區設定特有的。 如果物件建立延伸模組套用至所有地區設定，它必須在 DisplaySpecifiers 容器中所有地區設定子容器的物件類別 **displaySpecifier** 物件中註冊。 如果物件建立延伸模組已針對特定地區設定進行當地語系化，請在該地區設定的 subcontainer 中，將其註冊到 **displaySpecifier** 物件中。 如需 DisplaySpecifiers 容器和地區設定的詳細資訊，請參閱 [顯示](display-specifiers.md) 規範和 [DisplaySpecifiers 容器](displayspecifiers-container.md)。

有兩個 DisplaySpecifier 屬性可以在其中註冊物件建立延伸模組。 這些都是 **creationWizard** 和 **createWizardExt**。

**CreationWizard** 屬性會識別主要物件建立延伸模組，以取代 Active Directory 系統管理嵌入式管理單元中的現有或原生物件建立 wizard。主要建立延伸模組會提供第一組頁面，並以與原生頁面相同的方式來主控。 這個屬性是單一值，需要下列格式：


```C++
<CLSID>
```



" &lt; CLSID &gt; " 是 [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) 函式所產生之 COM 物件 CLSID 的字串表示。

**CreateWizardExt** 屬性會識別次要物件建立延伸模組。 次要建立延伸模組會將 wizard 頁面新增至原生頁面或主要延伸模組。 這個屬性是多重值，需要下列格式：


```C++
<order number>,<CLSID>
```



「 &lt; 訂單編號」 &gt; 是一種不帶正負號的數位，表示頁面在 wizard 中的位置。 顯示建立嚮導時，系統會使用每個值的「訂單編號」比較來排序這些值 &lt; &gt; 。 如果有一個以上的值具有相同的「 &lt; 訂單編號」 &gt; ，這些頁面會以從 Active Directory 伺服器讀取的順序載入。 可能的話，您應該使用非現有的「 &lt; 訂單編號」 &gt; (也就是，屬性) 中的其他值尚未使用的號碼。 沒有指定的開始位置，而且「訂單編號」序列中允許有間距 &lt; &gt; 。

" &lt; CLSID &gt; " 是 [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) 函式所產生之 COM 物件 CLSID 的字串表示。

 

 