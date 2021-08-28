---
description: Patch 物件的 SourceListInfo 屬性會取得並設定 patch 的來源資訊屬性。 這個屬性會呼叫 MsiSourceListGetInfo 或 MsiSourceListSetInfo。 這是讀取或寫入屬性。
ms.assetid: a07f2cc8-fee2-4703-89ea-769921713268
title: SourceListInfo 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9832fbe811f012932e4fb96bb8f530c4fc49d614ed5960c9f94065388f373833
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534438"
---
# <a name="patchsourcelistinfo-property"></a>SourceListInfo 屬性

[**Patch**](patch-object.md)物件的 **SourceListInfo** 屬性會取得並設定 patch 的來源資訊屬性。 這個屬性會呼叫 [**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa) 或 [**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)。 這是讀取或寫入屬性。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
propVal = Patch.SourceListInfo
```



## <a name="property-value"></a>屬性值

要查詢或設定之修補程式的來源資訊屬性名稱。 如需可能的值，請參閱本主題的「備註」一節。

## <a name="remarks"></a>備註

並非所有可抓取的屬性都可以設定。 *SzProperty* 參數可以是下列其中一個值。



| 屬性         | 可以設定嗎？ | 意義                                                                                                                                                                                                                                                           |
|------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MediaPackagePath | Y        | 相對於安裝媒體根目錄的路徑。                                                                                                                                                                                                          |
| DiskPrompt       | Y        | 提示使用者輸入安裝媒體時所用的提示範本。                                                                                                                                                                                          |
| LastUsedSource   | Y        | 修補程式最近使用的來源位置。 當您設定這個屬性時，請在來源位置前面加上網路來源的 "n;"，或輸入 "u;" 作為 URL 類型。 例如，使用 "n; \\ \\臨時 \\ \\ 測試 "或" u; https://microsoft.com/Patches/Office/SP1 "。 |
| LastUsedType     | N        | 如果最後使用的來源是網路位置，則為 "n"。 如果最後使用的來源是 URL 位置，則為 "u"。 如果最後使用的來源是媒體，則為 "m"。 空字串 ( "" ) 如果沒有最後使用的來源。                                                                      |
| PackageName      | Y        | 來源上 Windows Installer 封裝或修補封裝的名稱。                                                                                                                                                                                         |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | WindowsWindows Server 2012、Windows 8 Windows Server 2008 R2 或 Windows 7 上的安裝程式5.0。 WindowsWindows Server 2008 或 Windows Vista 上的安裝程式4.0 或 Windows Installer 4.5。 WindowsWindows Server 2003、Windows XP 和 Windows 2000 上的安裝程式3.0 或更新版本<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch 定義為000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListGetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistgetinfoa)
</dt> <dt>

[**MsiSourceListSetInfo**](/windows/desktop/api/Msi/nf-msi-msisourcelistsetinfoa)
</dt> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




