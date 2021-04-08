---
description: 提供壓縮圖片的圖片層級參數以進行 HEVC 影片解碼。
ms.assetid: F73AE9CD-5BBC-4A9F-8D05-707AD5E2E92A
title: 'DXVA_PicParams_HEVC 結構 (Dxva .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicParams_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: cafcbf31a7d4b7fee84e6c695f1d0f0a1e0302ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111781"
---
# <a name="dxva_picparams_hevc-structure"></a>DXVA \_ PicParams \_ HEVC 結構

提供壓縮圖片的圖片層級參數以進行 HEVC 影片解碼。

## <a name="syntax"></a>語法


```C++
typedef struct _DXVA_PicParams_HEVC {
  USHORT             PicWidthInMinCbsY;
  USHORT             PicHeightInMinCbsY;
  union {
    struct {
      USHORT chroma_format_idc  :2;
      USHORT separate_colour_plane_flag   :1;
      USHORT bit_depth_luma_minus8   :3;
      USHORT bit_depth_chroma_minus8  :3;
      USHORT log2_max_pic_order_cnt_lsb_minus4  :4;
      USHORT NoPicReorderingFlag   :1;
      USHORT  NoBiPredFlag   :1;
      USHORT ReservedBits1     :1;
    };
    USHORT  wFormatAndSequenceInfoFlags;
  };
  DXVA_PicEntry_HEVC CurrPic;
  UCHAR              sps_max_dec_pic_buffering_minus1;
  UCHAR              log2_min_luma_coding_block_size_minus3;
  UCHAR              log2_diff_max_min_luma_coding_block_size;
  UCHAR              log2_min_transform_block_size_minus2;
  UCHAR              log2_diff_max_min_transform_block_size;
  UCHAR              max_transform_hierarchy_depth_inter;
  UCHAR              max_transform_hierarchy_depth_intra;
  UCHAR              num_short_term_ref_pic_sets;
  UCHAR              num_long_term_ref_pics_sps;
  UCHAR              num_ref_idx_l0_default_active_minus1;
  UCHAR              num_ref_idx_l1_default_active_minus1;
  CHAR               init_qp_minus26;
  UCHAR              ucNumDeltaPocsOfRefRpsIdx;
  USHORT             wNumBitsForShortTermRPSInSlice;
  USHORT             ReservedBits2;
  union {
    struct {
      UINT32 scaling_list_enabled_flag  :1;
      UINT32 amp_enabled_flag  :1;
      UINT32 sample_adaptive_offset_enabled_flag  :1;
      UINT32 pcm_enabled_flag   :1;
      UINT32 pcm_sample_bit_depth_luma_minus1   :4;
      UINT32 pcm_sample_bit_depth_chroma_minus1     :4;
      UINT32 log2_min_pcm_luma_coding_block_size_minus3    :2;
      UINT32 log2_diff_max_min_pcm_luma_coding_block_size  :2;
      UINT32 pcm_loop_filter_disabled_flag  :1;
      UINT32 long_term_ref_pics_present_flag   :1;
      UINT32 sps_temporal_mvp_enabled_flag  :1;
      UINT32 strong_intra_smoothing_enabled_flag   :1;
      UINT32 dependent_slice_segments_enabled_flag    :1;
      UINT32 output_flag_present_flag   :1;
      UINT32 num_extra_slice_header_bits    :3;
      UINT32 sign_data_hiding_enabled_flag  :1;
      UINT32 cabac_init_present_flag  :1;
      UINT32 ReservedBits3    :5;
    };
    UINT32             dwCodingParamToolFlags;
    union {
      struct {
        UINT32 constrained_intra_pred_flag  :1;
        UINT32 transform_skip_enabled_flag  :1;
        UINT32 cu_qp_delta_enabled_flag  :1;
        UINT32 pps_slice_chroma_qp_offsets_present_flag  :1;
        UINT32 weighted_pred_flag  :1;
        UINT32 weighted_bipred_flag  :1;
        UINT32 transquant_bypass_enabled_flag  :1;
        UINT32 tiles_enabled_flag   :1;
        UINT32 entropy_coding_sync_enabled_flag   :1;
        UINT32 uniform_spacing_flag    :1;
        UINT32 loop_filter_across_tiles_enabled_flag   :1;
        UINT32 pps_loop_filter_across_slices_enabled_flag  :1;
        UINT32 deblocking_filter_override_enabled_flag  :1;
        UINT32 pps_deblocking_filter_disabled_flag  :1;
        UINT32 lists_modification_present_flag  :1;
        UINT32 slice_segment_header_extension_present_flag  :1;
        UINT32 IrapPicFlag  :1;
        UINT32 IdrPicFlag     :1;
        UINT32 IntraPicFlag   :1;
        UINT32 ReservedBits4     :13;
      };
      UINT32   dwCodingSettingPicturePropertyFlags;
    };
    CHAR               pps_cb_qp_offset;
    CHAR               pps_cr_qp_offset;
    UCHAR              num_tile_columns_minus1;
    UCHAR              num_tile_rows_minus1;
    USHORT             column_width_minus1[19];
    USHORT             row_height_minus1[21];
    UCHAR              diff_cu_qp_delta_depth;
    CHAR               pps_beta_offset_div2;
    CHAR               pps_tc_offset_div2;
    UCHAR              log2_parallel_merge_level_minus2;
    INT                CurrPicOrderCntVal;
    DXVA_PicEntry_HEVC RefPicList[15];
    UCHAR              ReservedBits5;
    INT                PicOrderCntValList[15];
    UCHAR              RefPicSetStCurrBefore[8];
    UCHAR              RefPicSetStCurrAfter[8];
    UCHAR              RefPicSetLtCurr[8];
    USHORT             ReservedBits6;
    USHORT             ReservedBits7;
    UINT               StatusReportFeedbackNumber;
  };
} DXVA_PicParams_HEVC, *PDXVA_PicParams_HEVC;
```



## <a name="members"></a>成員

<dl> <dt>

**PicWidthInMinCbsY**
</dt> <dd></dd> <dt>

**PicHeightInMinCbsY**
</dt> <dd></dd> <dt>

**色度 \_ 格式 \_ idc**
</dt> <dd></dd> <dt>

**個別的 \_ 色彩 \_ 平面 \_ 旗標** 
</dt> <dd></dd> <dt>

**位 \_ 深度 \_ luma \_ minus8** 
</dt> <dd></dd> <dt>

**位 \_ 深度 \_ 色度 \_ minus8**
</dt> <dd></dd> <dt>

**log2 \_ 最大的 \_ pic \_ 訂單 \_ cnt \_ lsb \_ minus4**
</dt> <dd></dd> <dt>

**NoPicReorderingFlag** 
</dt> <dd></dd> <dt>

 **NoBiPredFlag** 
</dt> <dd></dd> <dt>

**ReservedBits1** 
</dt> <dd></dd> <dt>

**wFormatAndSequenceInfoFlags**
</dt> <dd></dd> <dt>

**CurrPic**
</dt> <dd></dd> <dt>

**sps \_ 最大 \_ dec 的 \_ pic \_ 緩衝 \_ minus1**
</dt> <dd></dd> <dt>

**log2 \_ min \_ luma 程式 \_ 代碼 \_ 區塊 \_ 大小 \_ minus3**
</dt> <dd></dd> <dt>

**log2 \_ diff \_ 最 \_ 小 \_ luma \_ 編碼 \_ 區塊 \_ 大小**
</dt> <dd></dd> <dt>

**log2 \_ min \_ transform \_ block \_ size \_ minus2**
</dt> <dd></dd> <dt>

**log2 \_ 差異 \_ 最大 \_ 最小 \_ 轉換 \_ 區塊 \_ 大小**
</dt> <dd></dd> <dt>

**最大 \_ 轉換階層 \_ \_ 深度 \_ 間**
</dt> <dd></dd> <dt>

**最大 \_ 轉換階層 \_ \_ 深度 \_**
</dt> <dd></dd> <dt>

**\_短期 \_ \_ 參考 \_ pic \_ 組**
</dt> <dd></dd> <dt>

**\_長 \_ 詞彙 \_ 參考 \_ 圖片 \_ sps**
</dt> <dd></dd> <dt>

**num \_ ref \_ idx \_ l0 \_ 預設使用中 \_ \_ minus1**
</dt> <dd></dd> <dt>

**num \_ ref \_ idx \_ l1 \_ 預設使用中 \_ \_ minus1**
</dt> <dd></dd> <dt>

**init \_ qp \_ minus26**
</dt> <dd></dd> <dt>

**ucNumDeltaPocsOfRefRpsIdx**
</dt> <dd></dd> <dt>

**wNumBitsForShortTermRPSInSlice**
</dt> <dd></dd> <dt>

**ReservedBits2**
</dt> <dd></dd> <dt>

**調整 \_ 清單 \_ 啟用 \_ 旗標**
</dt> <dd></dd> <dt>

**amp \_ 啟用 \_ 旗標**
</dt> <dd></dd> <dt>

**範例調適型 \_ \_ 位移 \_ 已啟用 \_ 旗標**
</dt> <dd></dd> <dt>

**pcm \_ 啟用 \_ 旗標** 
</dt> <dd></dd> <dt>

**pcm \_ 範例 \_ 位 \_ 深度 \_ luma \_ minus1** 
</dt> <dd></dd> <dt>

**pcm \_ 範例 \_ 位 \_ 深度 \_ 色度 \_ minus1** 
</dt> <dd></dd> <dt>

**log2 \_ min \_ pcm \_ luma \_ 編碼 \_ 區塊 \_ 大小 \_ minus3** 
</dt> <dd></dd> <dt>

**log2 \_ diff \_ 最 \_ 小 \_ pcm \_ luma \_ 編碼 \_ 區塊 \_ 大小上限**
</dt> <dd></dd> <dt>

**pcm \_ 迴圈 \_ 篩選 \_ 停用 \_ 旗標**
</dt> <dd></dd> <dt>

**長期 \_ \_ 參考 \_ 圖片目前 \_ 的 \_ 旗標** 
</dt> <dd></dd> <dt>

**sps \_ 時態性 \_ mvp \_ 啟用 \_ 旗標**
</dt> <dd></dd> <dt>

**強 \_ 式 \_ \_ 啟用平滑啟用 \_ 旗標** 
</dt> <dd></dd> <dt>

**相依 \_ 磁區 \_ 區段 \_ 已啟用 \_ 旗標** 
</dt> <dd></dd> <dt>

**輸出 \_ 旗標 \_ 目前的 \_ 旗標** 
</dt> <dd></dd> <dt>

**\_額外的 \_ 磁區 \_ 標頭 \_ 位** 
</dt> <dd></dd> <dt>

**簽署 \_ 資料 \_ 隱藏 \_ 啟用 \_ 旗標**
</dt> <dd></dd> <dt>

**cabac \_ init \_ 存在 \_ 旗標**
</dt> <dd></dd> <dt>

**ReservedBits3** 
</dt> <dd></dd> <dt>

**dwCodingParamToolFlags**
</dt> <dd></dd> <dt>

**受限的 \_ 內部 \_ pred \_ 旗標**
</dt> <dd></dd> <dt>

**轉換 \_ 略過 \_ 啟用 \_ 旗標**
</dt> <dd></dd> <dt>

**cu \_ qp \_ delta \_ enabled \_ 旗標**
</dt> <dd></dd> <dt>

**pps \_ 配 \_ \_ 量色度 \_ qp \_ 有 \_ 旗標**
</dt> <dd></dd> <dt>

**加權 \_ pred \_ 旗標**
</dt> <dd></dd> <dt>

**加權 \_ bipred \_ 旗標**
</dt> <dd></dd> <dt>

**transquant \_ 略過 \_ 啟用 \_ 旗標**
</dt> <dd></dd> <dt>

**磚 \_ 已啟用 \_ 旗標** 
</dt> <dd></dd> <dt>

**\_ \_ 已啟用熵編碼同步 \_ \_ 旗標** 
</dt> <dd></dd> <dt>

**統一 \_ 間距 \_ 旗標** 
</dt> <dd></dd> <dt>

**\_ \_ 跨 \_ 磚 \_ 啟用 \_ 旗標的迴圈篩選** 
</dt> <dd></dd> <dt>

**\_跨配 \_ 量 \_ \_ \_ 啟用 \_ 旗標的 pps 迴圈篩選**
</dt> <dd></dd> <dt>

**deblocking \_ 篩選覆 \_ 寫 \_ 啟用 \_ 旗標**
</dt> <dd></dd> <dt>

**pps \_ deblocking \_ 濾波器 \_ disabled \_ 旗標**
</dt> <dd></dd> <dt>

**列出 \_ 修改 \_ 目前的 \_ 旗標**
</dt> <dd></dd> <dt>

**配量 \_ 區段 \_ 標題 \_ 延伸 \_ 顯示 \_ 旗標**
</dt> <dd></dd> <dt>

**IrapPicFlag**
</dt> <dd></dd> <dt>

**IdrPicFlag** 
</dt> <dd></dd> <dt>

**IntraPicFlag** 
</dt> <dd></dd> <dt>

**ReservedBits4** 
</dt> <dd></dd> <dt>

**dwCodingSettingPicturePropertyFlags**
</dt> <dd></dd> <dt>

**pps \_ cb \_ qp \_ offset**
</dt> <dd></dd> <dt>

**pps \_ cr 的 \_ qp \_ 位移**
</dt> <dd></dd> <dt>

**num \_ 圖格資料 \_ 行 \_ minus1**
</dt> <dd></dd> <dt>

**並排顯示的資料 \_ \_ 列 \_ minus1**
</dt> <dd></dd> <dt>

**資料行 \_ 寬度 \_ minus1**
</dt> <dd></dd> <dt>

**資料列 \_ 高度 \_ minus1**
</dt> <dd></dd> <dt>

**diff \_ cu \_ qp \_ delta \_ depth**
</dt> <dd></dd> <dt>

**pps \_ Beta \_ offset \_ div2**
</dt> <dd></dd> <dt>

**pps \_ tc \_ offset \_ div2**
</dt> <dd></dd> <dt>

**log2 \_ 平行 \_ 合併 \_ 層級 \_ minus2**
</dt> <dd></dd> <dt>

**CurrPicOrderCntVal**
</dt> <dd></dd> <dt>

**RefPicList**
</dt> <dd></dd> <dt>

**ReservedBits5**
</dt> <dd></dd> <dt>

**PicOrderCntValList**
</dt> <dd></dd> <dt>

**RefPicSetStCurrBefore**
</dt> <dd></dd> <dt>

**RefPicSetStCurrAfter**
</dt> <dd></dd> <dt>

**RefPicSetLtCurr**
</dt> <dd></dd> <dt>

**ReservedBits6**
</dt> <dd></dd> <dt>

**ReservedBits7**
</dt> <dd></dd> <dt>

**StatusReportFeedbackNumber**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8.1 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 R2 \[ desktop 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Dxva。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎結構](media-foundation-structures.md)
</dt> </dl>

 

 




