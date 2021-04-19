---
description: EXECUTEMODE 屬性會指定安裝程式執行系統更新的方式。
ms.assetid: 7b90d2e6-d661-412b-b054-2c218c95c02a
title: EXECUTEMODE 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ebf1de2fb7538ece838e674b62847f0c526842e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987987"
---
# <a name="executemode-property"></a>EXECUTEMODE 屬性

**EXECUTEMODE** 屬性會指定安裝程式執行系統更新的方式。 當需要執行安裝而不實際變更系統時，這個屬性可能很有用。 屬性可以設定為 [無] 以停用更新作業，例如安裝檔案和登錄值。

這個屬性可以是下列兩個值的其中之一。 安裝程式只會檢查值的第一個字母，並不區分大小寫。

<dl> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>沒有
</dt> <dd>

系統不會進行任何變更。 安裝程式會執行使用者介面，然後查詢資料庫。

</dd> <dt>

<span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>腳本
</dt> <dd>

系統會透過腳本執行來進行所有變更。 這是預設模式。

</dd> </dl>

## <a name="default-value"></a>預設值

如果未定義此屬性，執行模式會預設為腳本。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




