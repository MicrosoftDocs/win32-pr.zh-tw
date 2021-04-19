---
title: Install 元素
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 Install 元素會指定 Windows Media Player 用來安裝線上商店的值。
ms.assetid: 9a5e15ee-ec36-48d3-a1c2-bf20b6d2da48
keywords:
- Install 元素 Windows Media Player
topic_type:
- apiref
api_name:
- Install Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bba56240651f789b45c18b006b16e5e07b10676e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981102"
---
# <a name="install-element"></a>Install 元素

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**Install** 元素會指定 Windows Media Player 用來安裝線上商店的值。

``` syntax
<Install
    EULAURL = "URL"
    CodeURL = "URL"
    PrivacyInfoURL = "URL"
    InstallApp = "filename"
    InstallData = "commandline"
    CatalogURL = "URL"
/>
```

## <a name="attributes"></a>屬性

<dl> <dt>

<span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**EULAURL** (必要) 
</dt> <dd>

副檔名為 .txt 之檔案的完整 URL，Windows Media Player 用來顯示使用者授權合約 (EULA) 。 這個檔案必須以 ANSI 格式編碼。

</dd> <dt>

<span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**CodeURL** (必要) 
</dt> <dd>

封裝的完整 URL （副檔名為 .cab），可用來安裝線上存放區。 封裝和封裝中的所有程式碼模組都必須經過簽署。 如需程式碼簽署的詳細資訊，請參閱 MSDN Library 中的程式 [代碼簽署簡介](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) 。

</dd> <dt>

<span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**PrivacyInfoURL** (必要) 
</dt> <dd>

網頁的完整 URL，包含線上商店的隱私權原則資訊。

</dd> <dt>

<span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**InstallApp** (必要) 
</dt> <dd>

要執行之 EXE 或 INF 檔案的名稱。 這個檔案必須包含在 **CodeURL** 屬性所指定的 CAB 檔案中。

</dd> <dt>

<span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**InstallData** (選用) 
</dt> <dd>

傳遞給 **InstallApp** 屬性所指定之應用程式的命令列字串。 只有當 **InstallApp** 的值指定可執行檔時，才適用這個屬性。

</dd> <dt>

<span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>類型1所需的 **CatalogURL** (，已忽略類型 2) 
</dt> <dd>

線上商店編譯目錄的完整 URL。

</dd> </dl>

## <a name="parentchild-elements"></a>父/子項目



| 階層       | 元素         |
|-----------------|-----------------|
| 父元素 | **ServiceInfo** |
| 子元素  | 無            |



 

## <a name="remarks"></a>備註

如果任何必要的屬性遺失或無法使用，Windows Media Player 安裝程式將不會嘗試下載並安裝線上商店提供者程式碼。 安裝程式將會設定 **ServiceInfo** 檔中所指定的離線預設值。 **ServiceInfo** 可在未連線至網際網路的情況下使用，方法是將預設提供者名稱和 **ServiceInfo** 資訊當做命令列參數傳遞。 如需命令列選項的詳細資訊，請參閱轉散發 [Windows Media Player 軟體](redistributing-windows-media-player-software.md) 。

> [!Note]  
> 使用此專案時，您需要簽署與 Microsoft 的轉散發合約。 如需詳細資料，請洽詢您的業務代表。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------|
| 版本<br/> | Windows Media Player 10 或更新版本。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Type 2 線上商店的範例 ServiceInfo 檔**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo 檔**](serviceinfo-document.md)
</dt> </dl>

 

