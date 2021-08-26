---
description: '[轉換] 屬性是安裝套件時，安裝程式所套用的轉換清單。'
ms.assetid: da20f99e-3022-4382-97bb-8f1206072347
title: 轉換屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f873e439ef9542efa618a8e86c9667a3c962939f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474314"
---
# <a name="transforms-property"></a>轉換屬性

[ **轉換** ] 屬性是安裝套件時，安裝程式所套用的轉換清單。 安裝程式會依照它們在屬性中所列的順序來套用轉換。 轉換可以依其檔案名或完整路徑來指定。 若要指定多個轉換，請以分號分隔每個檔案名或完整路徑 (; ) 。 例如，若要將三個轉換套用至封裝，請將 **轉換** 設定為檔案名清單或完整路徑清單。

``` syntax
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
TRANSFORMS=\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst;\\server3\share3\path3\transform3.mst
```

您可以指定將轉換檔案內嵌在 .msi 檔案的儲存體中，而不是獨立的檔案，方法是在檔案名前面加上冒號 (： ) 。 例如，下列範例表示 transform1 和 transform2 都內嵌于 .msi 檔案中，而 transform3 則是獨立的檔案。

``` syntax
TRANSFORMS=:transform1.mst;:transform2.mst;transform3.mst
```

安裝程式需要在每次安裝、公告、隨選安裝或封裝的維護 **安裝中所** 列的轉換。 [TransformsSecure 原則](transformssecure-policy.md)原則、**轉換** 屬性和 **轉換** 字串的第一個字元會通知安裝程式如何處理獨立轉換檔案的來源復原。 Windows安裝程式會將設定 [TransformsAtSource 原則](transformsatsource-policy.md)或 [**TransformsAtSource**](transformsatsource.md)視為與 TransformsSecure 原則和 [**TransformsSecure**](transformssecure.md)相同。 請注意，內嵌在 .msi 檔案中的轉換並不會快取，而且一律會從封裝中取得。




| 轉換屬性 | 安全轉換 | 快取和復原 | 
|---------------------|-------------------|------------------------|
| @ [<em>檔案名的清單</em>] 範例：<br /> @transform1.mst; transform2 .mst;transform3 .mst<br /> | 沒有影響。 | <a href="secure-at-source-transforms.md">安全來源轉換</a>。 轉換的來源必須位於封裝來源的根目錄中。 安裝或公告封裝時，安裝程式會將使用者電腦上的轉換儲存在使用者沒有寫入存取權的快取中。 如果轉換的本機複本無法使用，安裝程式會搜尋來源以還原快取。 方法與搜尋 .msi 檔案的來源清單相同。 請參閱 <a href="source-resiliency.md">來源復原</a>。 | 
| |[<em>路徑清單</em>]例子：<br /><pre class="syntax" data-space="preserve"><code>|\\server\share\path\transform1.mst; \\server2\share2\path2\transform2.mst</code></pre> | 沒有影響。 | <a href="secure-full-path-transforms.md">安全-完整路徑轉換</a>。 每個轉換的來源都必須在傳遞至 <strong>轉換</strong>的完整路徑上。 轉換來源不一定要位於封裝的來源。 安裝或公告封裝時，安裝程式會將使用者電腦上的轉換儲存在使用者沒有寫入存取權的快取中。 如果轉換的本機複本無法使用，安裝程式只能從指定路徑的來源還原快取。 | 
| [<em>檔案名清單</em>]第一個字元不是 @ 或 |.<br /> 範例：<br /> transform1 .mst; transform2 .mst;transform3 .mst<br /> | <a href="transformssecure-policy.md">TransformsSecure 原則</a> 或 <a href="transformssecure.md"><strong>TransformsSecure</strong></a> 設定為1或<br /><a href="transformsatsource-policy.md">TransformsAtSource 原則</a> 或 <a href="transformsatsource.md"><strong>TransformsAtSource</strong></a> 設定為1。<br /> | 如果 <strong>轉換</strong> 是檔案名的清單，則安裝程式會將它們視為 <a href="secure-at-source-transforms.md">安全來源的轉換</a>。 如果 <strong>轉換</strong> 是完整路徑的清單，則安裝程式會將它們視為 <a href="secure-full-path-transforms.md">安全的完整路徑轉換</a>。<br /> | 
| [<em>檔案名清單</em>]第一個字元不是 @ 或 |.<br /> 範例：<br /> transform1 .mst; transform2 .mst;transform3 .mst<br /> | 未設定<a href="transformssecure-policy.md">TransformsSecure 原則</a>和<a href="transformssecure.md"><strong>TransformsSecure</strong></a><br />未設定<a href="transformsatsource-policy.md">TransformsAtSource 原則</a>和<a href="transformsatsource.md"><strong>TransformsAtSource</strong></a> 。<br /> | 不<a href="unsecured-transforms.md">安全的轉換</a>。 轉換的來源必須位於封裝來源的根目錄中。 當封裝已安裝或公告每位使用者時，安裝程式會將轉換儲存在使用者的設定檔中。 這可讓使用者在電腦之間漫遊，同時維持其自訂。 針對每部電腦安裝，轉換會儲存在%windir%\Installer 資料夾中。 如果轉換的本機複本無法使用，安裝程式會搜尋來源以還原快取。 方法與搜尋 .msi 檔案的來源清單相同。 請參閱 <a href="source-resiliency.md">來源復原</a>。 | 
| [<em>路徑清單</em>]第一個字元不是 @ 或 |.<br /> 範例：<br /><pre class="syntax" data-space="preserve"><code>\\server\share\path\transform1.mst;\\server2\share2\path2\transform2.mst.</code></pre> | 未設定<a href="transformsatsource-policy.md">TransformsAtSource 原則</a>和<a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a><br />未設定<a href="transformsatsource-policy.md">TransformsAtSource 原則</a>和<a href="transformssecure.md"><strong>TRANSFORMSSECURE</strong></a> 。<br /> | 不<a href="unsecured-transforms.md">安全的轉換</a>。 當封裝已安裝或公告每位使用者時，安裝程式會將轉換儲存在使用者的設定檔中。 這可讓使用者在電腦之間漫遊，同時維持其自訂。 針對每部電腦安裝，轉換會儲存在%windir%\Installer 資料夾中。 如果轉換的本機複本無法使用，安裝程式會搜尋來源以還原快取。 方法與搜尋 .msi 檔案的來源清單相同。 請參閱 <a href="source-resiliency.md">來源復原</a>。 | 




 

您無法在相同的 **轉換** 清單中同時使用檔案名和路徑。 您無法在相同清單中同時指定安全和設定檔轉換。 您可以將內嵌在套件中的轉換包含在具有其他轉換的清單中。

``` syntax
@transform1.mst;:transform2.mst 
|\\server\share\path\transform1.mst;:transform2.mst
```

請注意，因為轉換的清單分隔符號是分號字元，所以不能在轉換檔案名或路徑中使用分號。

## <a name="remarks"></a>備註

在使用 Windows Installer 設定 [TransformsSecure 原則](transformssecure-policy.md)或 [**TransformsSecure**](transformssecure.md)屬性的情況下， \| 使用命令列設定 **轉換** 時，不需要傳遞 @ 或符號。 如果清單完全是由位於來源的檔案名所組成，或者完全是由完整路徑所組成，則安裝程式會採用安全來源或安全的-完整路徑。 您仍然無法混用這兩種類型的轉換來源。

請注意，安裝程式會針對在第一次和維護安裝期間套用的不安全轉換使用不同的搜尋順序。 如需詳細資訊，請參閱不 [安全的轉換](unsecured-transforms.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003 或 Windows XP 上的安裝程式。 如需 Windows Installer 版本所需的最低 Windows service pack 相關資訊，請參閱[Windows Installer Run-Time 需求](windows-installer-portal.md)。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[資料庫轉換](database-transforms.md)
</dt> <dt>

[合併和轉換](merges-and-transforms.md)
</dt> <dt>

[來源復原](source-resiliency.md)
</dt> </dl>

 

 




