---
description: WsdCodeGen 有兩個函式：產生設定檔，以及產生 WSDAPI 用戶端和主機應用程式的原始程式碼。
ms.assetid: 75f5071c-040b-4e65-a80e-e1fea63535b0
title: WsdCodeGen 命令列語法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fff02fd9bbbcfddd20a68948f139e765d27a86363df12fc0057627717e53cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049636"
---
# <a name="wsdcodegen-command-line-syntax"></a>WsdCodeGen 命令列語法

WsdCodeGen 有兩個函式：產生設定檔，以及產生 WSDAPI 用戶端和主機應用程式的原始程式碼。 本主題提供用來執行每項工作的命令列語法。

## <a name="generating-a-configuration-file"></a>產生設定檔

### <a name="syntax"></a>Syntax

**WSDCODEGEN.EXE** **/generateconfig：**{**client** \| **host** \| **all**} **\[ /outputfile：**_ConfigFileName_ *_\]_* *WSDLFileNameList*

### <a name="parameters"></a>參數

<dl> <dt>

<span id="_generateconfig__client___host___all_"></span><span id="_GENERATECONFIG__CLIENT___HOST___ALL_"></span>**/generateconfig： {client \| host \| all}**
</dt> <dd>

輸出設定檔將產生的程式碼類型。 **/generateconfig：用戶端** 用來產生用來產生用戶端程式代碼的設定檔， **/generateconfig：主機** 可用來產生用來產生主機程式碼的設定檔，而 **/generateconfig： all** 用來產生設定檔，以產生用戶端和主機程式碼。

</dd> <dt>

<span id="_outputfile_ConfigFileName"></span><span id="_outputfile_configfilename"></span><span id="_OUTPUTFILE_CONFIGFILENAME"></span>**/outputfile：**_ConfigFileName_
</dt> <dd>

這個選擇性參數是用來指定輸出設定檔案的檔案名。 如果排除此參數，則會 codegen.config 輸出設定檔的名稱。

</dd> <dt>

<span id="_pnpx"></span><span id="_PNPX"></span>*/pnpx*
</dt> <dd>

在設定檔中包含 Pnp-x 範本。

</dd> <dt>

<span id="WSDLFileNameList"></span><span id="wsdlfilenamelist"></span><span id="WSDLFILENAMELIST"></span>*WSDLFileNameList*
</dt> <dd>

以空格分隔的 WSDL 檔案清單， (s) 要由 WsdCodeGen 處理。

</dd> </dl>

## <a name="generating-source-code"></a>產生原始程式碼

### <a name="syntax"></a>Syntax

**WSDCODEGEN.EXE** **/generatecode** **\[ /download \]** **\[ /gbc \]** **\[ outputroot：**_path_ *_\]_* **\[ /writeaccess：**_command_ *_\]_* *ConfigFileName*

### <a name="parameters"></a>參數

<dl> <dt>

<span id="_generatecode"></span><span id="_GENERATECODE"></span>**/generatecode**
</dt> <dd>

指示 WsdCodeGen 產生原始程式碼。 如果未指定任何模式，這就是預設模式。

</dd> <dt>

<span id="_download"></span><span id="_DOWNLOAD"></span>**/download**
</dt> <dd>

下載設定檔所參考的匯入檔。 這是選擇性參數。

</dd> <dt>

<span id="_gbc"></span><span id="_GBC"></span>**/gbc**
</dt> <dd>

將批註新增至表示產生程式碼的原始程式碼。 這些批註前面會加上「產生者」片語。 這是選擇性參數。

</dd> <dt>

<span id="_outputroot_path"></span><span id="_OUTPUTROOT_PATH"></span>**/outputroot：**_path_
</dt> <dd>

所產生檔案的輸出位置。 *路徑* 可以是絕對或相對路徑。 這是選擇性參數。

</dd> <dt>

<span id="_writeaccess_command"></span><span id="_WRITEACCESS_COMMAND"></span>**/writeaccess：**_命令_
</dt> <dd>

指示 WsdCodeGen 在修改磁片上的任何現有檔案之前，執行指定的命令。 與磁片上相同的輸出檔案不會收到此命令，也不會寫入這些檔案。 如果命令包含序列 " {0} "，此序列將會取代為要修改的檔案名。 如果沒有，則會將檔案名附加至命令。

範例：

**/writeaccess： "attrib-r"**

**/writeaccess： "attrib-r {0} "**

**/writeaccess： "copy {0} ... \\備份 \\ 」**

</dd> <dt>

<span id="ConfigFileName"></span><span id="configfilename"></span><span id="CONFIGFILENAME"></span>*ConfigFileName*
</dt> <dd>

產生程式碼之前要處理的設定檔名稱。

</dd> </dl>

## <a name="formatting-legend"></a>格式圖例



| 格式                                                                    | 意義                                                 |
|---------------------------------------------------------------------------|---------------------------------------------------------|
| *斜體*                                                                  | 使用者必須提供的資訊                  |
| **粗體字**                                                                  | 使用者必須依照顯示的方式鍵入的元素       |
| 介於括弧之間 (\[ \])                                                    | 選擇性項目                                          |
| 介於大括弧 ({}) ; 以管道 () 分隔的選項 \| 。 範例： {偶數 \| 奇數} | 使用者必須從中選擇一項的選項集 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[WsdCodeGen 設定檔](wsdcodegen-configuration-file.md)
</dt> <dt>

[使用 WsdCodeGen](using-wsdcodegen.md)
</dt> </dl>

 

 




