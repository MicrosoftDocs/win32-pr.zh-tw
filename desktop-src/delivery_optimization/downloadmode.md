---
title: 'DownloadMode 列舉 (>deliveryoptimization) '
description: 定義傳遞最佳化使用的不同下載模式。
ms.assetid: 7E9407C6-A22F-459E-B316-5E7809F0067A
keywords:
- 略過「傳遞最佳化」並改用 BITS。 例如，選取此模式即可讓用戶端使用 BranchCache。 列舉型別
topic_type:
- apiref
api_name:
- DownloadMode
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ea753ef47dc2e6655d7e707466d7b0448bee7bec1f090b1baf4de04799283d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543722"
---
# <a name="downloadmode-enumeration"></a>DownloadMode 列舉

定義傳遞最佳化使用的不同下載模式。

## <a name="syntax"></a>Syntax


```C++
typedef enum _DownloadMode { 
  DownloadMode_CdnOnly   = 0,
  DownloadMode_Lan       = 1,
  DownloadMode_Group     = 2,
  DownloadMode_Internet  = 3,
  DownloadMode_Simple    = 99,
  DownloadMode_Bypass    = 100
} DownloadMode;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**
</dt> <dd>

此設定會停用對等快取，但仍可讓傳遞最佳化從 Microsoft 伺服器下載內容。 此模式會使用「傳遞最佳化」雲端服務所提供的其他中繼資料，達到無對等、可靠且有效率的下載體驗。

</dd> <dt>

<span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**
</dt> <dd>

這個預設的「傳遞最佳化」操作模式可啟用相同網路上的對等共用。

</dd> <dt>

<span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**
</dt> <dd>

當設定群組模式時，系統會根據裝置的 Active Directory Domain Services (AD DS) 網站 (Windows 10、1607版) 或裝置驗證的網域，以 (Windows 10 1511 版) 來自動選取群組。 在群組模式中，會跨內部子網路、在屬於相同群組的裝置 (包括遠端辦公室中的裝置) 之間進行對等互連。 您可以使用 GroupID 選項來建立自己的自訂群組，而不受網域和 AD DS 網站影響。 對於大部分組織而言，若要透過「傳遞最佳化」實現頻寬最佳化，建議使用群組下載模式的選項。

</dd> <dt>

<span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**
</dt> <dd>

針對「傳遞最佳化」啟用網際網路對等來源。

</dd> <dt>

<span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**
</dt> <dd>

簡單模式會完全停用「傳遞最佳化」雲端服務 (針對離線環境)。 當「傳遞最佳化」雲端服務無法使用、無法連線或當內容檔案大小小於 10 MB 時，「傳遞最佳化」會自動切換成這種模式。 在此模式下，「傳遞最佳化」會在沒有對等快取下提供可靠的下載體驗。

</dd> <dt>

<span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**
</dt> <dd>

略過「傳遞最佳化」並改用 BITS。 例如，選取此模式即可讓用戶端使用 BranchCache。

</dd> </dl>

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-------------------------------|----------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>      |
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>  |
| 標頭<br/>                   | <dl> <dt>>Deliveryoptimization。h</dt> </dl>               |
