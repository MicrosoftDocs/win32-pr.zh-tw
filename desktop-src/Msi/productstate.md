---
description: 安裝程式會在初始化時將 ProductState 屬性設定為產品的安裝狀態。
ms.assetid: 833e9a15-10f8-4b1c-945f-bc02b506f627
title: ProductState 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51ea88058aa8bae6b67acaea96b506a7560c7a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994918"
---
# <a name="productstate-property"></a>ProductState 屬性

安裝程式會在初始化時將 **ProductState** 屬性設定為產品的安裝狀態。 這個屬性會設定為下列其中一個 [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)所傳回的 INSTALLSTATE 資料類型。



| INSTALLSTATE             | 數值 | 產品的安裝狀態                   |
|--------------------------|---------------|-------------------------------------------------|
| INSTALLSTATE \_ 不明    | -1            | 未公告或安裝產品。 |
| INSTALLSTATE \_ 公告 | 1             | 產品已公告但未安裝。    |
| INSTALLSTATE 不 \_ 存在     | 2             | 已針對不同的使用者安裝產品。  |
| INSTALLSTATE \_ 預設值    | 5             | 已為目前使用者安裝產品。  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003 或 Windows XP 上的 Windows Installer。 如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性](properties.md)
</dt> </dl>

 

 




