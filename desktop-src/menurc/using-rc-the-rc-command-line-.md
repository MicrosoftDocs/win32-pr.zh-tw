---
title: 使用 RC (RC 命令列)
description: 若要啟動 RC，請使用下列命令。
ms.assetid: da087e15-ecb5-4d03-b534-be872cf7d8b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34e24fdf7b9b648a9baf9c6db8981f05d5434ef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933166"
---
# <a name="using-rc-the-rc-command-line"></a>使用 RC (RC 命令列)

若要啟動 RC，請使用下列命令。

**RC** \[*選項* \]*腳本-file*

*腳本* 檔案參數會指定資源定義檔的名稱，其中包含要編譯之資源的名稱、類型、檔案名和描述。

RC 可以針對同時具有非語言相關和語言專屬資源的應用程式，產生個別的資源檔。 開發人員可以使用 [資源設定檔](/windows/desktop/Intl/preparing-resources) 案或設定命令列選項，來選取哪些資源類型和專案是非當地語系化的 [語言 (LN) ](/windows/desktop/Intl/mui-resource-management) 檔案的不可當地語系化資源，以及哪些是特定語言的 MUI 檔案的可當地語系化資源。 如需詳細資訊，請參閱 [多語系消費者介面](/windows/desktop/Intl/multilingual-user-interface)。

*Options* 參數可以是下列一或多個命令列選項。

## <a name="options"></a>選項

<dl> <dt>

<span id="__"></span>**/?**
</dt> <dd>

顯示命令列選項的清單。

</dd> <dt>

<span id="_c"></span><span id="_C"></span>**/c**
</dt> <dd>

定義 NLS 轉換所使用的字碼頁。

</dd> <dt>

<span id="_d"></span><span id="_D"></span>**/d**
</dt> <dd>

定義預處理器的符號，您可以使用 [**\# ifdef**](-ifdef.md)指示詞進行測試。

</dd> <dt>

<span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/fm** *mresname*
</dt> <dd>

RC 會建立一個語言中立的。RES 檔案和與語言相依 (MUI) 。使用 *指令檔的* RES 檔案。 此選項必須與 **/fo** *resname* 選項一起使用。 RC 會以非語言相關的名稱來命名。RES file *resname* 和 language 相依 (MUI) 的名稱。RES file *mresname .res*。

**Windows Server 2003 和 WINDOWS XP/2000：** 此選項無法使用，也不會在更新的系統上使用 [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) 和 [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) 函數。

</dd> <dt>

<span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/fo** *resname*
</dt> <dd>

RC 會建立。使用腳本檔案名稱為 *resname* *的* RES 檔案。

如果同時設定了 **/fm** *MRESNAME* 選項，RC 就會建立一個非語言相關。RES 檔案和與語言相依 (MUI) 。RES 檔。

**Windows Server 2003 和 WINDOWS XP/2000：** 此選項無法使用，也不會在更新的系統上使用 [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) 和 [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) 函數。

</dd> <dt>

<span id="_g1"></span><span id="_G1"></span>**/g1**
</dt> <dd>

如果設定了/g1，則當 MUI 檔案中唯一包含的可當地語系化資源是版本資源時，RC 會產生 MUI 檔案。 如果未設定/g1，則如果 MUI 檔中唯一包含的可當地語系化資源是版本資源，RC 將不會產生 MUI 檔案。

</dd> <dt>

<span id="_h"></span><span id="_H"></span>**/h**
</dt> <dd>

顯示命令列選項的清單。

</dd> <dt>

<span id="_I"></span><span id="_i"></span>**/I**
</dt> <dd>

搜尋指定的目錄，然後搜尋 INCLUDE 環境變數所指定的目錄。

</dd> <dt>

<span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *loctype*
</dt> <dd>

可當地語系化的資源類型 RC 會放入與語言相依的 (MUI) 。RES 檔。 如果 **/q** 選項也已設定，則會忽略此選項，且 RC 設定檔中的資訊會優先。

**Windows Server 2003 和 WINDOWS XP/2000：** 此選項無法使用，也不會在更新的系統上使用 [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) 和 [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) 函數。

</dd> <dt>

<span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** 的 *改寫*
</dt> <dd>

RC 同時放入非語言相關的重迭資源類型。RES 和與語言相依的 (MUI) 。RES 檔。 **/K** 選項所指定的資源類型必須是 **/j** 選項所指定的子集。 例如，？J2?J3 接?K3 指定 RC 會在語言中性和語言相依 (MUI) 檔中放置資源類型3。 如果 **/q** 選項也已設定，則會忽略此選項，且 RC 設定檔中的資訊會優先。

**Windows Server 2003 和 WINDOWS XP/2000：** 此選項無法使用，也不會在更新的系統上使用 [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) 和 [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) 函數。

</dd> <dt>

<span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *langid*
</dt> <dd>

指定編譯的預設語言。 例如，-l409 相當於在資源腳本檔案的頂端包含下列語句： `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`

如需詳細資訊，請參閱 [語言識別項](/windows/desktop/Intl/language-identifiers)。

</dd> <dt>

<span id="_n"></span><span id="_N"></span>**n**
</dt> <dd>

Null 會終止字串資料表中的所有字串。

</dd> <dt>

<span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/Q** *Mui. RCConfig*
</dt> <dd>

遵循 RC 設定檔案格式的 RC 設定檔案。 RC 設定檔案格式可讓元件自行描述資源的資訊，例如資源版本控制、MUI 檔案路徑、資源類型和專案。 此檔案會指定哪些資源要進入非語言相關。RES 檔案，以及哪些資源會進入與語言相依的 (MUI) 。RES 檔。 此選項以及 RC 設定檔中提供的資訊，會覆寫命令列選項 **/j** 和 **/k**。

**Windows Server 2003 和 WINDOWS XP/2000：** 此選項無法使用，也不會在更新的系統上使用 [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) 和 [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) 函數。

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

忽略。 為了與現有的 makefile 相容而提供。

</dd> <dt>

<span id="_u"></span><span id="_U"></span>**u**
</dt> <dd>

取消預處理器的符號。

</dd> <dt>

<span id="_v"></span><span id="_V"></span>**/v**
</dt> <dd>

顯示報告編譯器進度的訊息。

</dd> <dt>

<span id="_x"></span><span id="_X"></span>**/x**
</dt> <dd>

在搜尋標頭檔或資源檔時，防止 RC 檢查 INCLUDE 環境變數。

</dd> </dl>

## <a name="remarks"></a>備註

選項不區分大小寫，且 ( ) 的連字號可以用來取代 (/) 的斜線符號。 如果不需要任何額外的參數，您可以結合單字母選項。

RC 不會在下列情況下產生 MUI 檔案。

-   .Rc 檔中沒有可當地語系化的資源存在。
-   .Rc 檔中唯一指定的資源語言識別項是中性 (0x0) 。
-   .Rc 檔中的資源會以一種以上的語言指定。 例外狀況是，如果 .rc 檔包含兩種語言，而其中一種語言為中性 (0x0) ，RC 會產生 MUI 檔案。

如需詳細資訊，請參閱下列主題：

-   [定義預處理器的名稱](defining-names-for-the-preprocessor.md)
-   [重新命名已編譯的資源檔](renaming-the-compiled-resource-file.md)
-   [搜尋檔案](searching-for-files.md)
-   [顯示進度訊息](displaying-progress-messages.md)
-   [RC 診斷訊息](rc-diagnostic-messages.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[多語系使用者介面](/windows/desktop/Intl/multilingual-user-interface)
</dt> </dl>

 

 