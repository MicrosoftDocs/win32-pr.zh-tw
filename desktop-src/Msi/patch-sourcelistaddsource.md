---
description: SourceListAddSource 方法會新增網路或 URL 來源。 接受 SourcePath、Type 和 Index 作為參數。 這個方法會呼叫 MsiSourceListAddSourceEx。
ms.assetid: 87797a8c-f1ba-4bfb-9296-3d3ef2a3c37f
title: SourceListAddSource 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cc0a3bc0d966ec6836d1523745b296350562aaa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987088"
---
# <a name="patchsourcelistaddsource-method"></a>SourceListAddSource 方法

**SourceListAddSource** 方法會新增網路或 URL 來源。 接受 *SourcePath*、 *Type* 和 *Index* 作為參數。 這個方法會呼叫 [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)。

## <a name="syntax"></a>語法


```JScript
Patch.SourceListAddSource(
  Type,
  SourcePath,
  Index
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*型別* 
</dt> <dd>

要新增的來源類型： MSISOURCETYPE \_ NETWORK 或 MSISOURCETYPE \_ URL。

</dd> <dt>

*SourcePath* 
</dt> <dd>

要加入之來源的路徑。

</dd> <dt>

*Index* 
</dt> <dd>

如果呼叫 **SourceListAddSource** 時，新的來源和 *索引* 設定為0，則安裝程式會將來源加入至來源清單的結尾。

如果使用來源清單中已存在的來源來呼叫此函數，而且 *索引* 設定為0，則安裝程式會保留來源的現有索引。

如果函式是使用來源清單中的現有來源來呼叫，且 *索引* 設定為非零值，則會從清單中的目前位置移除來源，並將其插入 *索引* 所指定的位置，然後再插入至該位置已存在的任何來源。

如果函式是以新的來源呼叫，且 *索引* 設定為非零值，則會在該位置已存在的任何來源之前，將來源插入 *索引* 所指定的位置。 在 *索引* 所指定的索引之後，清單中所有來源的索引值都會更新，以確保唯一的索引值，而預先存在的訂單仍維持不變。

如果 *索引* 大於清單中的來源數目，則會將來源放在清單結尾，且索引值大於任何現有來源。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。 Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。 Windows Server 2003、Windows XP 及 Windows 2000 上的 Windows Installer 3.0 或更新版本<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch 定義為000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




