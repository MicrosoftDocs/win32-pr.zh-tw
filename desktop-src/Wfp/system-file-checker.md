---
description: 系統檔案檢查程式的 Sfc.exe，可讓系統管理員掃描所有受保護的資源，以驗證其版本。
ms.assetid: 72f69ad2-15d9-4191-a8aa-4c23a2392006
title: 系統檔案檢查程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4e0d67f6de6aba62fe262969d7f30db0c45335
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981218"
---
# <a name="system-file-checker"></a>系統檔案檢查程式

系統檔案檢查程式的 Sfc.exe，可讓系統管理員掃描所有受保護的資源，以驗證其版本。

重新開機不符合預期 Windows 版本之 Windows 的重要檔案，可能會以正確的版本取代。 如果檔案已修復，則也會修復對應的登錄資料。 未修復受保護的檔案不是重新開機 Windows 的關鍵。

## <a name="syntax"></a>Syntax

以下是 Sfc 的命令列語法。

**SFC 選項 \[ = 完整檔案路徑\]**

## <a name="options"></a>選項

<dl> <dt>

<span id="_CACHESIZE_x"></span><span id="_cachesize_x"></span><span id="_CACHESIZE_X"></span>/CACHESIZE =*x*
</dt> <dd>

不支援這個值。

**Windows Server 2003 和 WINDOWS XP：** 設定檔案快取大小。 快取的預設大小為 0x32 (50 MB) 。

</dd> <dt>

<span id="_CANCEL"></span><span id="_cancel"></span>/CANCEL
</dt> <dd>

不支援這個值。

</dd> <dt>

<span id="_ENABLE"></span><span id="_enable"></span>/ENABLE
</dt> <dd>

不支援這個值。

</dd> <dt>

<span id="_FILESONLY"></span><span id="_filesonly"></span>/FILESONLY
</dt> <dd>

確認或只修復檔案。 請勿確認或修復登錄機碼。

**WINDOWS XP：** 不支援。

</dd> <dt>

<span id="_OFFBOOTDIR"></span><span id="_offbootdir"></span>/OFFBOOTDIR
</dt> <dd>

使用此選項可進行離線修復。 指定離線開機目錄的位置。

**WINDOWS XP：** 不支援。

</dd> <dt>

<span id="_OFFWINDIR"></span><span id="_offwindir"></span>/OFFWINDIR
</dt> <dd>

使用此選項可進行離線修復。 指定離線 Windows 目錄的位置。

**WINDOWS XP：** 不支援。

</dd> <dt>

<span id="_PURGECACHE"></span><span id="_purgecache"></span>/PURGECACHE
</dt> <dd>

不支援這個值。

**Windows Server 2003 和 WINDOWS XP：** 清空檔案快取，並掃描所有受保護的系統檔案。

</dd> <dt>

<span id="_QUIET"></span><span id="_quiet"></span>/QUIET
</dt> <dd>

不支援這個值。

</dd> <dt>

<span id="_REVERT"></span><span id="_revert"></span>/REVERT
</dt> <dd>

返回預設設定。

**Windows Server 2008 和 Windows Vista：** 不支援。

</dd> <dt>

<span id="_SCANBOOT"></span><span id="_scanboot"></span>/SCANBOOT
</dt> <dd>

不支援這個值。

**Windows Server 2003 和 WINDOWS XP：** 每次開機時掃描所有受保護的系統檔案。

</dd> <dt>

<span id="_SCANFILE"></span><span id="_scanfile"></span>/SCANFILE
</dt> <dd>

掃描並修復位於指定完整路徑的檔案。

**WINDOWS XP：** 不支援。

</dd> <dt>

<span id="_SCANNOW"></span><span id="_scannow"></span>/SCANNOW
</dt> <dd>

立即掃描所有受保護的系統檔案。

</dd> <dt>

<span id="_SCANONCE"></span><span id="_scanonce"></span>/SCANONCE
</dt> <dd>

不支援這個值。

**Windows Server 2003 和 WINDOWS XP：** 在下一次開機時掃描所有受保護的系統檔案。

</dd> <dt>

<span id="_VERIFYFILE"></span><span id="_verifyfile"></span>/VERIFYFILE
</dt> <dd>

驗證位於指定完整路徑的檔案。 此選項不會修復檔案。

**WINDOWS XP：** 不支援。

</dd> <dt>

<span id="_VERIFYONLY"></span><span id="_verifyonly"></span>/VERIFYONLY
</dt> <dd>

掃描所有受保護的系統檔案，但不修復檔案。

**WINDOWS XP：** 不支援。

</dd> </dl>

Sfc 會設定下列登錄值：

 = HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCScan

如需詳細資訊，請參閱 [WFP 登錄值](wfp-registry-values.md)。

## <a name="remarks"></a>備註

在 Windows Vista 中，您可以將 **windows \_ 追蹤 \_** 記錄檔環境變數設為有效目錄的位置，以接收記錄檔。

## <a name="examples"></a>範例

下列範例命令列是 sfc.exe 語法的範例。

**sfc/SCANNOW**

**sfc/VERIFYFILE = c： \\ windows \\ system32 \\kernel32.dll**

**sfc/SCANFILE = d： \\ windows \\ system32 \\kernel32.dll/OFFBOOTDIR = d： \\ /OFFWINDIR = d： \\ windows**

**sfc/VERIFYONLY/FILESONLY**

 

 



