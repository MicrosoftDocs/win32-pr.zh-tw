---
description: SOURCELIST 屬性是應用程式安裝套件的網路或 URL 來源路徑清單（以分號分隔）。
ms.assetid: 9dc1e195-a108-4f8f-b008-e08fc7658fc0
title: SOURCELIST 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5384504c337aeb9f1848f59efb2c6abaee5887b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977599"
---
# <a name="sourcelist-property"></a>SOURCELIST 屬性

**SOURCELIST** 屬性是應用程式安裝套件的網路或 URL 來源路徑清單（以分號分隔）。 這份清單會附加到應用程式的每個使用者現有來源清單的結尾。 安裝程式會藉由列舉來源路徑清單來找出來源，並使用它所找到的第一個可存取位置。 只有此來源可用於安裝的其餘部分。 因此，來源清單中指定的每個路徑都必須是具有應用程式完整來源的位置。 每個來源位置的整個目錄樹狀結構必須相同，而且必須包含所有必要的來源檔案，包括任何封包。 每個位置都必須有一個具有相同檔案名和產品代碼的 .msi 檔案。

## <a name="default-value"></a>預設值

如果產品尚未公告或安裝，則安裝程式只會檢查 **SOURCELIST** 屬性。 在所有其他情況下，安裝程式會使用登錄中的現有來源清單。

## <a name="remarks"></a>備註

使用 **SOURCELIST** 屬性加入的來源會直接加入至每個來源類型的清單結尾，而且一律會在 [**SourceDir**](sourcedir.md) 屬性指定的預設來源之後。

針對 Windows Installer **SOURCELIST** 屬性中的來源數目是無限制的。 [**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea) 可以用來新增網路來源。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> <dt>

[來源復原](source-resiliency.md)
</dt> </dl>

 

 




